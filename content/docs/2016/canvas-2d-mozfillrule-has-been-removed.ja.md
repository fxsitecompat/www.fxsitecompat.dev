---
title: "Canvas 2D `mozFillRule` が削除されました"
date: "2016-08-11T00:41:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=826619"
      title: "Bug 826619 - Unprefix mozFillRule"
aliases:
    - "/ja/docs/2016/canvasrenderingcontext2d-mozfillrule-has-been-removed/"
---
廃止予定となっていた `CanvasRenderingContext2D.mozFillRule` プロパティが、[`fill`](https://developer.mozilla.org/ja/docs/Web/API/CanvasRenderingContext2D/fill) メソッドの標準化された `fillRule` 引数に取って代わられる形で削除されました。`ctx.mozFillRule = "evenodd"` は単純に `ctx.fill("evenodd")` と書き換えられます。
