---
title: "`getElementsByTagName` が `tagName` ではなく `localName` に一致するようになりました"
date: "2015-10-23T02:32:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=492933": "Bug 492933 - getElementsByTagName should match on localName not tagName (for interop)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1236329": "Bug 1236329 - Error on HP Deskjet 2540 printer configuration page"
---
[`Document.getElementsByTagName`](https://developer.mozilla.org/ja/docs/Web/API/document/getElementsByTagName)、[`Element.getElementsByTagName`](https://developer.mozilla.org/ja/docs/Web/API/Element/getElementsByTagName) 両メソッドが、最新の仕様に従い、ノードの [`tagName`](https://developer.mozilla.org/ja/docs/Web/API/Element/tagName) プロパティに代わって [`localName`](https://developer.mozilla.org/ja/docs/Web/API/Node/localName) プロパティに一致するようになりました。

この変更は `<svg:circle>` のように XML 名前空間接頭辞が付いたノードに影響します。この例では、`getElementsByTagName('svg:circle')` はノードに一致しなくなり、`getElementsByTagName('circle')` で代用可能です。ただし、[`getElementsByTagNameNS`](https://developer.mozilla.org/ja/docs/Web/API/Document/getElementsByTagNameNS) メソッドがより正式で推奨されることから、`getElementsByTagNameNS('http://www.w3.org/2000/svg', 'circle')` のように書き換えられるでしょう。

この変更により、一部 *HP* プリンタの設定ページが動作しなくなっているようです。
