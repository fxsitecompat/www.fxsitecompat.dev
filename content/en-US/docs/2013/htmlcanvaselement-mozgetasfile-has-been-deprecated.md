---
title: "`HTMLCanvasElement.mozGetAsFile` has been deprecated"
date: "2013-09-19T23:58:13-04:00"
categories: ["canvas-webgl", "dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=803612": "Bug 803612 – Add deprecation warnings for mozGetAsFile"
---
The non-standard `mozGetAsFile` method on the [`HTMLCanvasElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement) interface is now deprecated and will be removed soon. The standard `toBlob` method can be used instead.
