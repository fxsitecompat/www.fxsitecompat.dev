---
title: "Service Worker Cache API によっていくつかのグローバルオブジェクトが追加されました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=940273": "Bug 940273 - Implement Cache and CacheStorage for ServiceWorkers"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1110144": "Bug 1110144 - ship Service Worker Cache in release builds"
---
[Service Worker](https://developer.mozilla.org/ja/docs/Web/API/ServiceWorker_API) の Cache API が Firefox 39 より初期設定で有効となりました。この API は新しい [`Cache`](https://developer.mozilla.org/ja/docs/Web/API/Cache)、[`CacheStorage`](https://developer.mozilla.org/ja/docs/Web/API/CacheStorage) 両インタフェースを提供するため、今後これらの名前を独自のグローバル変数に使うことはできません。
