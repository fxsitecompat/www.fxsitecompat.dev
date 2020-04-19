---
title: "`localName`、`namespaceURI`、`prefix` プロパティが `Node` から `Element` へ移されました"
date: "2016-04-24T01:37:00-04:00"
categories: ["dom"]
tags: []
versions: ["48", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1055776"
      title: "Bug 1055776 - Investigate moving namespaceURI, prefix, and localName to Element and Attr"
---
[`Node`](https://developer.mozilla.org/docs/Web/API/Node) インターフェイス上の [`localName`](https://developer.mozilla.org/docs/Web/API/Element/localName)、[`namespaceURI`](https://developer.mozilla.org/docs/Web/API/Node/namespaceURI)、[`prefix`](https://developer.mozilla.org/docs/Web/API/Node/prefix) プロパティが、最近の DOM 仕様に従い、[`Element`](https://developer.mozilla.org/docs/Web/API/Element)、[`Attr`](https://developer.mozilla.org/docs/Web/API/Attr) 両インターフェイスへ移動されました。他のノード上ではこれらのプロパティはすべて `undefined` を返すようになります。Chrome 48 が既にこの変更を行っていることから、大きな互換性問題は発生しないでしょう。
