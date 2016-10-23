---
title: "`SVGDocument` が削除されました"
date: "2016-10-05T07:06:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293786"
      title: "Bug 1293786 - Remove SVGDocument"
---
`SVGDocument` インターフェイスが、SVG 2 仕様に存在しなくなったため削除されました。SVG ドキュメントのタイプは [`XMLDocument`](https://developer.mozilla.org/ja/docs/Web/API/XMLDocument) に変わります。`rootElement` プロパティは [`Document`](https://developer.mozilla.org/ja/docs/Web/API/Document) インターフェイスへ移されたため、引き続き使用可能です。
