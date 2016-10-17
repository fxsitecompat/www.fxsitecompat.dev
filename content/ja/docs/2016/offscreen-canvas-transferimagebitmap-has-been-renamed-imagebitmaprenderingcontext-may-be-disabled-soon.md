---
title: "オフスクリーン Canvas の `transferImageBitmap()` が改名され、`ImageBitmapRenderingContext` は近々無効化される見通しです"
date: "2016-10-12T13:40:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1304767"
      title: "Bug 1304767 - Rename transferImageBitmap to transferFromImageBitmap"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1307628"
      title: "Bug 1307628 - Consider unshipping bitmaprender context."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/C27bDUacM3o/discussion"
      title: "Intent to unship: Canvas ImageBitmapRenderingContext"
---
[`ImageBitmapRenderingContext.transferImageBitmap`](https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmapRenderingContext/transferImageBitmap) メソッドが、最新の仕様に従って `transferFromImageBitmap` に改名されました。 古いメソッドは廃止予定となり、近い将来削除されます。

なお、[`ImageBitmapRenderingContext`](https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmapRenderingContext) インタフェース自体、Firefox 46 で誤って出荷されたことが明らかになりました。オフスクリーン Canvas API はまだ鋭意開発中であることから、仕様が安定するのを待つため、この実装は近々無効化される可能性があります。まだ他のどのブラウザもこの新たな API を出荷していないため、リスクは非常に低いはずです。
