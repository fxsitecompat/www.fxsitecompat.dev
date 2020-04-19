---
title: "`HTMLElement` メンバーが継承チェーンのすべてに継承されなくなりました"
date: "2012-12-29T08:29:30-05:00"
categories: ["dom"]
tags: []
versions: ["20", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=821606"
      title: "Bug 821606 – Turn on WebIDL bindings for Element and HTMLElement"
---
従来、リーフクラスのインターフェイスプロトタイプオブジェクト上で継承チェーン (例: [`HTMLDivElement`](https://developer.mozilla.org/docs/Web/API/HTMLDivElement) → [`HTMLElement`](https://developer.mozilla.org/docs/Web/API/HTMLElement) → [`Element`](https://developer.mozilla.org/docs/Web/API/Element) → [`Node`](https://developer.mozilla.org/docs/Web/API/Node) → [`EventTarget`](https://developer.mozilla.org/docs/Web/API/EventTarget)) 全体のすべてのメンバーを取得することが可能でしたが (例: `HTMLDivElement.prototype === document.createElement("div").__proto`)、今後 [`HTMLElement`](https://developer.mozilla.org/docs/Web/API/HTMLElement) のメンバーは `HTMLElement.prototype` (`=== HTMLDivElement.prototype.__proto__`) だけにとどまります。

少なくともひとつの人気ライブラリ ([Optimizely](https://www.optimizely.com/)) がこの誤った挙動に依存していることが分かりました。ライブラリ側で既に修正が行われていますので、ウェブサイトでこのライブラリを使っている場合は必ず最新版に更新してください。

[`DOMString`](https://developer.mozilla.org/docs/DOM/DOMString) 引数を取るメソッドに `null` を渡すと、空文字列の代わりに `"null"` という文字列に変換されるようになりました。例えば、`element.setAttribute("foo", null)` とした場合、`<div foo="">` ではなく `<div foo="null">` という出力になります。

[`DOMParser`](https://developer.mozilla.org/docs/DOM/DOMParser) の `parseFromStream`、`parseFromBuffer` メソッド、[`XMLSerializer`](https://developer.mozilla.org/docs/XMLSerializer) の `serializeToStream` メソッドは廃止予定となり、コンテンツ上では使用できなくなりました。クローム＝拡張機能のコードでは引き続き使用可能です。
