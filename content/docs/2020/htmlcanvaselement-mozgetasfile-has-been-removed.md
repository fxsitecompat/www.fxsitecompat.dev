---
title: "`HTMLCanvasElement.mozGetAsFile()` has been removed"
date: "2020-01-20T20:22:00-05:00"
categories: ["canvas-webgl", "dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1588980"
      title: "Bug 1588980 - Unship HTMLCanvasElement.mozGetAsFile()"
---
The non-standard `mozGetAsFile` method on the [`HTMLCanvasElement`](https://developer.mozilla.org/docs/Web/API/HTMLCanvasElement) interface, deprecated since [Firefox 26](https://www.fxsitecompat.dev/en-CA/docs/2013/htmlcanvaselement-mozgetasfile-has-been-deprecated/), has been removed with Firefox 74. Use the standard `toBlob` method instead.
