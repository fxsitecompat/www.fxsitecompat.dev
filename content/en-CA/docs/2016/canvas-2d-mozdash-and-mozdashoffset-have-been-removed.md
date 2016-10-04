---
title: "Canvas 2D `mozDash` and `mozDashOffset` have been removed"
date: "2016-10-04T11:26:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=931389"
      title: "Bug 931389 - Deprecate and remove CanvasRenderingContext2D.mozDash/mozDashOffset"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/UIudMABegcY/discussion"
      title: "Intent to unship: canvas 2D context mozDash and mozDashOffset."
---
The support for the non-standard, deprecated `CanvasRenderingContext2D.mozDash` and `mozDashOffset` properties have been removed with Firefox 52. Use the standardized [`getLineDash`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/getLineDash) and [`setLineDash`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/setLineDash) methods instead of the `mozDash` property. The [`lineDashOffset`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineDashOffset) property is the standard equivalent of `mozDashOffset`.
