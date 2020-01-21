---
title: "`HTMLCanvasElement.mozGetAsFile()` has been deprecated"
date: "2013-09-19T23:58:13-04:00"
categories: ["canvas-webgl", "dom"]
tags: []
versions: ["26"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=803612"
      title: "Bug 803612 – Add deprecation warnings for mozGetAsFile"
---
The non-standard `mozGetAsFile` method on the [`HTMLCanvasElement`](https://developer.mozilla.org/docs/Web/API/HTMLCanvasElement) interface is now deprecated and will be removed soon. The standard `toBlob` method can be used instead.

**Update**: The method has been removed with [Firefox 74](https://www.fxsitecompat.dev/en-CA/docs/2020/htmlcanvaselement-mozgetasfile-has-been-removed/).
