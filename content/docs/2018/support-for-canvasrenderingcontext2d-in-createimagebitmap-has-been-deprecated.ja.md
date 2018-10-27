---
title: "`createImageBitmap()` における `CanvasRenderingContext2D` 対応が廃止予定となりました"
date: "2018-10-27T00:09:00-04:00"
categories: ["canvas-webgl", "dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1502304"
      title: "Bug 1502304 - Deprecated CanvasRenderingContext2D in CreateImageBitmap"
---
[`createImageBitmap`](https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/createImageBitmap) メソッドは `<img>`、`<video>`、`Blob` など様々な種類の画像ソースを受け付けます。Firefox は [`CanvasRenderingContext2D`](https://developer.mozilla.org/docs/Web/API/CanvasRenderingContext2D) も受け付けますが、これは仕様になく、他のどのブラウザーも対応していません。この非標準の挙動は廃止予定となり、近い将来削除されることとなりました。代わりに `<canvas>` を直接使用してください。
