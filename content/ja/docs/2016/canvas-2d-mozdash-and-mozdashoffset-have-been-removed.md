---
title: "Canvas 2D の `mozDash` と `mozDashOffset` が削除されました"
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
非標準で廃止予定となっていた `CanvasRenderingContext2D.mozDash`、`mozDashOffset` 両プロパティへの対応が Firefox 52 で削除されました。`mozDash` プロパティの代わりに標準化された [`getLineDash`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/getLineDash)、[`setLineDash`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/setLineDash) 両メソッドを使用してください。`mozDashOffset` の標準版は [`lineDashOffset`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/lineDashOffset) プロパティとなります。
