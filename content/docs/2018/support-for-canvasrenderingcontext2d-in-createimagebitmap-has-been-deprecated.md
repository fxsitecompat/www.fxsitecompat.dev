---
title: "Support for `CanvasRenderingContext2D` in `createImageBitmap()` has been deprecated"
date: "2018-10-27T00:09:00-04:00"
categories: ["canvas-webgl", "dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1502304"
      title: "Bug 1502304 - Deprecated CanvasRenderingContext2D in CreateImageBitmap"
---
The [`createImageBitmap`](https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/createImageBitmap) method accepts various types of image sources including an `<img>`, `<video>` and `Blob`. Firefox accepts a [`CanvasRenderingContext2D`](https://developer.mozilla.org/docs/Web/API/CanvasRenderingContext2D) as well, but it's not in the spec nor supported by any other browser. This non-standard behaviour is now considered deprecated and will be removed in the near future. Use a `<canvas>` directly instead.
