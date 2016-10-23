---
title: "`<textarea>` 上の間違った `padding` 実装が修正されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["css"]
tags: []
versions: ["29"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=157846"
      title: "Bug 157846 – Incorrect implementation of padding on textarea elements (scrollbars/resizer wrongly positioned)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1012202"
      title: "Bug 1012202 – eBay Messages: textarea is expanded while typing due to the scrollHeight change with Firefox 29"
---
これまで Firefox は [`<textarea>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/textarea) 要素上の [`padding`](https://developer.mozilla.org/ja/docs/Web/CSS/padding) を正しく実装していませんでしたが、これが修正され、[このスクリーンショットが示す通り](https://bug157846.bugzilla.mozilla.org/attachment.cgi?id=784647) 長年にわたるブラウザー互換性の問題が解決しました。CSS 仕様と他のブラウザーの挙動に合わせ、`padding` のスペースは、スクロールバーとリサイズコントロールの外側ではなく内側へ追加されるようになりました。

`padding` は、その要素上の [`clientWidth`](https://developer.mozilla.org/ja/docs/Web/API/Element.clientWidth)、[`clientHeight`](https://developer.mozilla.org/ja/docs/Web/API/Element.clientHeight)、[`scrollWidth`](https://developer.mozilla.org/ja/docs/Web/API/Element.scrollWidth)、[`scrollHeight`](https://developer.mozilla.org/ja/docs/Web/API/Element.scrollHeight) プロパティにも含まれます。この変更による副作用が *eBay* で発見され、メッセージテキストエリアの高さが文字入力中に自動的に拡大する機能に影響が出ていました。
