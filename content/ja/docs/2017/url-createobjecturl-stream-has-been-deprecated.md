---
title: "`URL.createObjectURL(stream)` が廃止予定となりました"
date: "2017-02-02T22:38:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["54"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1334564"
      title: "Bug 1334564 - Deprecate and remove URL.createObjectURL(mediastream)"
---
開発者間の議論の結果、Firefox とその他のブラウザーは、[`URL.createObjectURL`](https://developer.mozilla.org/ja/docs/Web/API/URL/createObjectURL) 静的メソッドのオブジェクト引数に [`MediaStream`](https://developer.mozilla.org/ja/docs/Web/API/MediaStream) を受け入れることを近々中止することになりました。Firefox 54 では、そのようなコードが見つかった場合、コンソールに廃止予定の警告が表示されます。

[仕様に書かれている例](https://w3c.github.io/mediacapture-main/#examples) が示す通り、`<video>` あるいは `<audio>` 要素上に `MediaStream` を設定するには、[`HTMLMediaElement.prototype.srcObject`](https://developer.mozilla.org/ja/docs/Web/API/HTMLMediaElement/srcObject) プロパティを使ってください。

```js
// 非推奨
video.src = URL.createObjectURL(stream);
// 推奨
video.srcObject = stream;
```
