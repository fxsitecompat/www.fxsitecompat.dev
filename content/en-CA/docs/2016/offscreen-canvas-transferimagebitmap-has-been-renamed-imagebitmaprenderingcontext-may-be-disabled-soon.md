---
title: "Offscreen Canvas `transferImageBitmap()` has been renamed; `ImageBitmapRenderingContext` may be disabled soon"
date: "2016-10-12T13:40:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304767"
      title: "Bug 1304767 - Rename transferImageBitmap to transferFromImageBitmap"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1307628"
      title: "Bug 1307628 - Consider unshipping bitmaprender context."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/C27bDUacM3o/discussion"
      title: "Intent to unship: Canvas ImageBitmapRenderingContext"
---
The [`ImageBitmapRenderingContext.transferImageBitmap`](https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmapRenderingContext/transferImageBitmap) method has been renamed to `transferFromImageBitmap` in order to follow the latest spec. The old one is now deprecated and will be removed in the near future.

Also, it becomes obvious that the [`ImageBitmapRenderingContext`](https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmapRenderingContext) interface itself has been accidentally shipped with Firefox 46. Since the Offscreen Canvas API is still under active development, the implementation may soon be disabled to wait until the spec is stabilized. No other browsers have shipped the new API, so that the risk should be very low.
