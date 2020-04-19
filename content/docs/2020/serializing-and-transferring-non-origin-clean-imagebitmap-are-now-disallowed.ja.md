---
title: "オリジンが純粋でない `ImageBitmap` のシリアライズと転送が禁止されました"
date: "2020-02-10T23:07:00-05:00"
categories: ["dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1604694"
      title: "Bug 1604694 - Disallow serializing and transferring non-origin-clean ImageBitmap"
    - url: "https://groups.google.com/a/chromium.org/d/topic/blink-dev/Z1XdYf6SjDU/discussion"
      title: "Intent to Deprecate and Remove: non-origin-clean ImageBitmap serialization and transferring"
---
[`ImageBitmap`](https://developer.mozilla.org/docs/Web/API/ImageBitmap) は [Cross-Origin Resource Sharing](https://developer.mozilla.org/docs/Web/HTTP/CORS) (CORS) メカニズムによって検証されていないクロスオリジン画像からのデータを含む可能性があります。Firefox 74 および [Chrome 80](https://www.chromestatus.com/feature/5728790883860480) 以降、セキュリティ上の理由から、そうした `ImageBitmap` のシリアライズや転送が不可能となります。開発者によればこれはめったに使われない機能であることから、互換性への影響は軽微なはずです。
