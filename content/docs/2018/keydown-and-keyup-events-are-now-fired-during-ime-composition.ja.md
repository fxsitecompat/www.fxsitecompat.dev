---
title: "IME 変換中にも `keydown`、`keyup` イベントが発生するようになりました"
date: "2018-12-11T09:03:00-05:00"
categories: ["dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=354358"
      title: "Bug 354358 - keydown/keyup events should be dispatched even during composition (but keypress shouldn't be so)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1446401"
      title: "Bug 1446401 - Start to dispatch keydown/keyup events even during composition in Nightly and early Beta"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496288"
      title: "Bug 1496288 - Ship Window.event, keyCode change, and keypress event handling changes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oZEz5JH9ZK8/discussion"
      title: "Intent to ship: Start to dispatch \"keydown\" and \"keyup\" events even if composing (only in Nightly and early Beta)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DrYa0gDxI5Q/discussion"
      title: "Intent to ship: dispatching \"keydown\" and \"keyup\" events during IME composition"
aliases:
    - "/ja/docs/2018/keydown-and-keyup-events-will-soon-be-fired-during-ime-composition/"
---
[UI Events 仕様](https://w3c.github.io/uievents/) や他のブラウザーの挙動に合わせるため、Firefox は、[インプットメソッドエディター](https://ja.wikipedia.org/wiki/%E3%82%A4%E3%83%B3%E3%83%97%E3%83%83%E3%83%88%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89) (IME) による変換中にも `keydown`、`keyup` 両イベントの発生を行うようにしました。IME ヘルパーアプリケーションは、中国、日本、韓国、台湾 (CJKT) の人たちによって文字入力欄に母国語のマルチバイト文字を入力するために使われます。

従来、例えば日本語で「絵」と入力したい場合、以下のようなイベントが発生していました。

1. `keydown { isComposing: false, key: "e", keyCode: 69 }`
1. `compositionstart { data: "" }`
3. `compositionupdate { data: "え" }`
4. `input { isComposing: true }`
5. `compositionupdate { data: "絵" }`
6. `input { isComposing: true }`
7. `compositionend { data: "絵" }`
8. `input { isComposing: false }`
9. `keyup { isComposing: false, key: "Enter", keyCode: 13 }`

Firefox 65 以降、これは以下のようになります。

1. `keydown { isComposing: false, key: "Process", keyCode: 229 }`
2. `compositionstart { data: "" }`
3. `compositionupdate { data: "え" }`
4. `input { isComposing: true }`
5. `keyup { isComposing: true, key: "e", keyCode: 69 }`
6. `keydown { isComposing: true, key: "Process", keyCode: 229 }`
7. `compositionupdate { data: "絵" }`
8. `input { isComposing: true }`
9. `keyup { isComposing: true, key: " ", keyCode: 32 }`
10. `keydown { isComposing: true, key: "Process", keyCode: 229 }`
11. `compositionend { data: "絵" }`
12. `input { isComposing: false }`
13. `keyup { isComposing: false, key: "Enter", keyCode: 13 }`

ちなみに、英語で「e」と入力した場合、4 つのイベントしか発生しません。

1. `keydown { isComposing: false, key: "e", keyCode: 69 }`
2. `keypress { isComposing: false }`
3. `input { isComposing: false }`
4. `keyup { isComposing: false, key: "e", keyCode: 69 }`

お気付きの通り、変換中 `key` プロパティは `"Process"` となり、[`compositionstart`](https://developer.mozilla.org/docs/Web/Events/compositionstart) と [`compositionend`](https://developer.mozilla.org/docs/Web/Events/compositionend) イベントの間は [`isComposing`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/isComposing) プロパティも `true` となります。つまり、変換中に何もしたくない場合は、以下のように `keydown`、`keyup` あるいは `input` イベントリスナーの中で単純に `isComposing` をチェックしてください。

```js
$input.addEventListener('keydown', event => {
  if (event.isComposing) {
    return;
  }
  // 何か処理を行います
});
```

この新たな挙動は Firefox 61 以降 Nightly と早期 Beta/DevEdition チャンネルでは有効化されていました。ウェブアプリケーション開発者の皆さんには、自分のアプリをテストし、それが CJKT ユーザーにとって正常に動作し続けるよう確認することをお勧めします。より詳しい実装メモは Mozilla の国際化エンジニアによる [ニュースグループへの投稿](https://groups.google.com/d/topic/mozilla.dev.platform/oZEz5JH9ZK8/discussion) を参照してください。
