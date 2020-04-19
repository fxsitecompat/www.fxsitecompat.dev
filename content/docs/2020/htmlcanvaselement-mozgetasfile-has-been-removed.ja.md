---
title: "`HTMLCanvasElement.mozGetAsFile()` が廃止されました"
date: "2020-01-20T20:22:00-05:00"
categories: ["canvas-webgl", "dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1588980"
      title: "Bug 1588980 - Unship HTMLCanvasElement.mozGetAsFile()"
---
[Firefox 26](https://www.fxsitecompat.dev/ja/docs/2013/htmlcanvaselement-mozgetasfile-has-been-deprecated/) 以降廃止予定となっていた [`HTMLCanvasElement`](https://developer.mozilla.org/docs/Web/API/HTMLCanvasElement) インターフェイス上の非標準の `mozGetAsFile` メソッドが Firefox 74 で廃止されました。代わりに標準の `toBlob` メソッドを使ってください。
