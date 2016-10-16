---
title: "特定の Canvas テキスト効果が正しく描画されません"
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
[`CanvasRenderingContext2D.filter`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/filter)、[`globalAlpha`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/globalAlpha)、[`globalCompositeOperation`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation)、[`shadowBlur`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/shadowBlur) の各プロパティが、[`fillText`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/fillText) メソッドでのテキスト描画時に反映されないというリグレッションが Firefox 49 で発生しました。これらのバグは Firefox 49.0.2 で修正されました。
