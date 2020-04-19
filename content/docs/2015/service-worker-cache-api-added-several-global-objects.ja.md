---
title: "Service Worker Cache API によっていくつかのグローバルオブジェクトが追加されました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
releases: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=940273"
      title: "Bug 940273 - Implement Cache and CacheStorage for ServiceWorkers"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1110144"
      title: "Bug 1110144 - ship Service Worker Cache in release builds"
---
[Service Worker](https://developer.mozilla.org/docs/Web/API/ServiceWorker_API) の Cache API が Firefox 39 より初期設定で有効となりました。この API は新しい [`Cache`](https://developer.mozilla.org/docs/Web/API/Cache)、[`CacheStorage`](https://developer.mozilla.org/docs/Web/API/CacheStorage) 両インターフェイスおよびグローバル [`caches`](https://developer.mozilla.org/docs/Web/API/WorkerGlobalScope/caches) プロパティを提供するため、今後これらの名前を独自のグローバル変数に使うことはできません。
