---
title: "`SVGZoomEvent` が削除されました"
date: "2017-04-05T16:56:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1314388"
      title: "Bug 1314388 - Remove SVGZoomEvent"
---
SVG 2 仕様から除外された [`SVGZoomEvent`](https://www.w3.org/TR/SVG/script.html#InterfaceSVGZoomEvent) インターフェイスとイベント、そのバリエーションである `SVGZoomEvents`、`<svg>` ルート要素向け `onzoom` 要素への対応が Firefox 55 で削除されました。
