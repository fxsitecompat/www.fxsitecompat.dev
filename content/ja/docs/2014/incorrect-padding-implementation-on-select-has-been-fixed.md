---
title: "`<select>` 上の間違った `padding` 実装が修正されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["css"]
tags: []
versions: "30"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=963970": "Bug 963970 – Arrow of drop-down list should not be affected by padding"
---
[`<select>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/select) 要素上の [`padding`](https://developer.mozilla.org/ja/docs/Web/CSS/padding) について Firefox が抱えていた誤実装が修正されました。この変更によって `padding` のスペースはドロップダウンリストの外側でなく内側に追加され、CSS の仕様や他のブラウザの挙動に一致するようになります。この問題は、[Firefox 29 で修正](https://www.fxsitecompat.com/ja/docs/2014/incorrect-padding-implementation-on-textarea-has-been-fixed/) された [`<textarea>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/textarea) 要素上の同じ問題に開発者が取り組んでいる間に発見されました。`multiple` 属性付きの `<select>` 要素はこの変更による影響を受けません。

`-moz-appearance:none` を使ってドロップダウンリストの矢印を隠すハックは、[矢印のスタイリングを可能にして欲しいという要求](https://bugzilla.mozilla.org/show_bug.cgi?id=649849) はあるものの、機能しなくなります。すべてのブラウザ上でドロップダウンリストのデザインを完全に制御したいページ作者は、代わりに独自要素を作成すべきでしょう。
