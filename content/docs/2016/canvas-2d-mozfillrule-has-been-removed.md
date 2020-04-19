---
title: "Canvas 2D `mozFillRule` has been removed"
date: "2016-08-11T00:41:00-04:00"
categories: ["canvas-webgl"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=826619"
      title: "Bug 826619 - Unprefix mozFillRule"
aliases:
    - "/en-CA/docs/2016/canvasrenderingcontext2d-mozfillrule-has-been-removed/"
---
The deprecated `CanvasRenderingContext2D.mozFillRule` property has been removed in favour of the standardized `fillRule` parameter for the [`fill`](https://developer.mozilla.org/docs/Web/API/CanvasRenderingContext2D/fill) method. `ctx.mozFillRule = "evenodd"` can be simply replaced with `ctx.fill("evenodd")`.
