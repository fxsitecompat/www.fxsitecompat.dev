---
title: "今後 IME 変換中にも `keydown`、`keyup` イベントが発生するようになります"
date: "2018-05-07T16:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1446401"
      title: "Bug 1446401 - Start to dispatch keydown/keyup events even during composition in Nightly and early Beta"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oZEz5JH9ZK8/discussion"
      title: "Intent to ship: Start to dispatch \"keydown\" and \"keyup\" events even if composing (only in Nightly and early Beta)"
---
近い将来、[UI Events 仕様](https://w3c.github.io/uievents/) や他のブラウザーの挙動に合わせるため、Firefox は [インプットメソッドエディター](https://ja.wikipedia.org/wiki/%E3%82%A4%E3%83%B3%E3%83%97%E3%83%83%E3%83%88%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89) (IME) による変換中にも `keydown`、`keyup` 両イベントの発生を行うようにします。IME ヘルパーアプリケーションは、中国、日本、韓国、台湾 (CJKT) の人たちによって文字入力欄に母国語のマルチバイト文字を入力するために使われます。

Firefox の現行版では、例えば日本語で「絵」と入力したい場合、以下のようなイベントが発生します。

1. `keydown { isComposing: false, key: "e", keyCode: 69 }`
1. `compositionstart { data: "" }`
3. `compositionupdate { data: "え" }`
4. `input { isComposing: true }`
5. `compositionupdate { data: "絵" }`
6. `input { isComposing: true }`
7. `compositionend { data: "絵" }`
8. `input { isComposing: false }`
9. `keyup { isComposing: false, key: "Enter", keyCode: 13 }`

将来のバージョンでは、これは以下のようになります。

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

ちなみに、英語で「e」と入力した場合、3 つのイベントしか発生しません。

1. `keydown { isComposing: false, key: "e", keyCode: 69 }`
2. `input { isComposing: false }`
3. `keyup { isComposing: false, key: "e", keyCode: 69 }`

お気付きの通り、変換中 `key` プロパティは `"Process"` となり、[`compositionstart`](https://developer.mozilla.org/ja/docs/Web/Events/compositionstart) と [`compositionend`](https://developer.mozilla.org/ja/docs/Web/Events/compositionend) イベントの間は [`isComposing`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent/isComposing) プロパティも `true` となります。つまり、変換中に何もしたくない場合は、以下のように `keydown`、`keyup` あるいは `input` イベントリスナーの中で単純に `isComposing` をチェックしてください。

```js
$input.addEventListener('keydown', event => {
  if (event.isComposing) {
    return;
  }
  // 何か処理を行います
});
```

この新たな挙動は Firefox 61 以降 Nightly と早期 Beta/DevEdition チャンネルでは既に有効化されています。ウェブアプリケーション開発者の皆さんには [プレリリース版](https://www.mozilla.org/ja/firefox/channel/desktop/) のいずれかでテストし、CJKT ユーザーにとってアプリが正常に動作し続けるよう確認することをお勧めします。より詳しい実装メモは Mozilla の国際化エンジニアによる [ニュースグループへの投稿](https://groups.google.com/d/topic/mozilla.dev.platform/oZEz5JH9ZK8/discussion) を参照してください。
