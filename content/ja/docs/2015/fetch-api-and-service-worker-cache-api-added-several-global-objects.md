---
title: "Fetch API と Service Worker Cache API によっていくつかのグローバルオブジェクトが追加されました"
date: "2015-03-17T14:02:59-04:00"
categories: ["dom"]
tags: []
versions: ["39"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1133861"
      title: "Bug 1133861 - Enable the Fetch API by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1143306"
      title: "Bug 1143306 - Missing contents of http://www.dailymotion.com/video/"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=940273"
      title: "Bug 940273 - Implement Cache and CacheStorage for ServiceWorkers"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1146557"
      title: "Bug 1146557 - enable Service Worker Cache pref for non-release builds"
---
Firefox 39 以降、新しい [Fetch API](https://developer.mozilla.org/ja/docs/Web/API/Fetch_API) が初期設定で有効となっています。この API によって [`Headers`](https://developer.mozilla.org/ja/docs/Web/API/Headers)、[`Request`](https://developer.mozilla.org/ja/docs/Web/API/Request)、[`Response`](https://developer.mozilla.org/ja/docs/Web/API/Response) インタフェースと [`fetch`](https://developer.mozilla.org/ja/docs/Web/API/GlobalFetch/fetch) メソッドが実装されたため、今後これらの名前を独自のグローバル変数に使うことはできません。*Dailymotion* のサイトが、独自の `Request` オブジェクトを使用していたことから、この変更による影響を受けたことが判明しています。

Firefox 39 では [Service Worker](https://developer.mozilla.org/ja/docs/Web/API/ServiceWorker_API) の Cache API も実装され、Aurora、Nightly 両チャンネルで有効化されていますので、新しい [`Cache`](https://developer.mozilla.org/ja/docs/Web/API/Cache)、[`CacheStorage`](https://developer.mozilla.org/ja/docs/Web/API/CacheStorage) インタフェースにも注意すべきでしょう。
