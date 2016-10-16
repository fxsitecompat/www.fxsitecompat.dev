---
title: "Specific Canvas text effects are not rendered properly"
date: "2016-10-03T16:54:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304539"
      title: "Bug 1304539 - Canvas fillText / strokeText do not respect canvas filters"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304353"
      title: "Bug 1304353 - HTML5 Canvas globalAlpha has no effect on fillText in Firefox.49"
aliases:
    - "/docs/2016/canvas-2d-globalalpha-and-globalcompositeoperation-have-no-effect-on-filltext/"
---
Firefox 49 introduced a regression where the [`CanvasRenderingContext2D.filter`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/filter), [`globalAlpha`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalAlpha), [`globalCompositeOperation`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation) and [`shadowBlur`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/shadowBlur) properties were not honoured when rendering text using the [`fillText`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fillText) method. These bugs have been fixed with Firefox 49.0.2.
