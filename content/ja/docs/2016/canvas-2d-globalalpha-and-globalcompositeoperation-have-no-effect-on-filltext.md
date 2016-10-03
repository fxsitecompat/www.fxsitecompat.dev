---
title: "Canvas 2D の `globalAlpha` と `globalCompositeOperation` が `fillText` に対して効果がありません"
date: "2016-10-03T16:54:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304353"
      title: "Bug 1304353 - HTML5 Canvas globalAlpha has no effect on fillText in Firefox.49"
---
[`CanvasRenderingContext2D.globalAlpha`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/globalAlpha)、[`globalCompositeOperation`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation) 両プロパティが、[`fillText`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/fillText) メソッドでのテキスト描画時に反映されないというリグレッションが Firefox 49 で発生しました。このバグは Firefox 50 で修正されました。
