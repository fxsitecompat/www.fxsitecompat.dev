---
title: "`SVGNumber` のコンストラクターが廃止されました"
date: "2018-04-25T12:33:00-04:00"
categories: ["dom", "svg"]
tags: []
releases: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455940"
      title: "Bug 1455940 - Remove constructor from SVGNumber"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/1jEXK-Ctbng/discussion"
      title: "Intent to unship constructors on SVGNumber"
---
[`SVGNumber`](https://developer.mozilla.org/docs/Web/API/SVGNumber) インターフェイス上のコンストラクターが Firefox 61 で削除されました。これは SVG 仕様に含まれておらず、他のどのブラウザーにも実装されていません。今後 `new SVGNumber()` を呼び出すと `TypeError` が投げられます。
