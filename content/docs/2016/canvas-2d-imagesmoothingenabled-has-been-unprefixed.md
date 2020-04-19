---
title: "Canvas 2D `imageSmoothingEnabled` has been unprefixed"
date: "2016-09-04T01:23:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=768072"
      title: "Bug 768072 - Implement imageSmoothingEnabled and deprecate mozImageSmoothingEnabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1228850"
      title: "Bug 1228850 - Remove mozImageSmoothingEnabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Nv4efVxrhCo/discussion"
      title: "Intent to ship/unprefix: Canvas2D imageSmoothingEnabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ozygu09pg_o/discussion"
      title: "Intent to ship imageSmoothingEnabled and remove mozImageSmoothingEnabled."
---
The [`CanvasRenderingContext2D.imageSmoothingEnabled`](https://developer.mozilla.org/docs/Web/API/CanvasRenderingContext2D/imageSmoothingEnabled) property has been unprefixed with Firefox 51. The deprecated `moz`-prefixed property will be warned in the console and removed in the future.
