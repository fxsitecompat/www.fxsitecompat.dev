---
title: "Canvas 2D `globalAlpha` and `globalCompositeOperation` have no effect on `fillText`"
date: "2016-10-03T16:54:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304353"
      title: "Bug 1304353 - HTML5 Canvas globalAlpha has no effect on fillText in Firefox.49"
---
Firefox 49 introduced a regression where the [`CanvasRenderingContext2D.globalAlpha`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalAlpha) and [`globalCompositeOperation`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation) properties were not honoured when rendering text using the [`fillText`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fillText) method. This bug has been fixed with Firefox 50.
