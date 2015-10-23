---
title: "`setAttributeNode` で作成され名前に大文字を含む属性について `getAttribute` が `null` を返します"
date: "2015-10-22T22:14:00-07:00"
categories: ["dom"]
tags: []
versions: ["38"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1165851": "Bug 1165851 - document.createAttribute can not get their own Added attributes"
---
Firefox 38 で、仕様準拠のため [`Element.setAttributeNode`](https://developer.mozilla.org/ja/docs/Web/API/Element/setAttributeNode) メソッドの実装が変更されました。その副作用として、属性が `setAttributeNode` で作成、[`NamedNodeMap.setNamedItem`](https://developer.mozilla.org/ja/docs/Web/API/NamedNodeMap/setNamedItem) で設定され、1 文字以上の大文字が属性名に含まれる場合に、[`Element.getAttribute`](https://developer.mozilla.org/ja/docs/Web/API/Element/getAttribute) メソッドがその属性にアクセスできず `null` を返します。いくつかのサイトに影響があったため、この問題は元の変更を Firefox 39 からバックアウトする形で修正されました。
