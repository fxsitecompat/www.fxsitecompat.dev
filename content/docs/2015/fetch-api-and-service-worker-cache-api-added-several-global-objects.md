---
title: "Fetch API and Service Worker Cache API added several global objects"
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
Starting with Firefox 39, the new [Fetch API](https://developer.mozilla.org/docs/Web/API/Fetch_API) has been enabled by default. This API has implemented the [`Headers`](https://developer.mozilla.org/docs/Web/API/Headers), [`Request`](https://developer.mozilla.org/docs/Web/API/Request), [`Response`](https://developer.mozilla.org/docs/Web/API/Response) interfaces as well as the [`fetch`](https://developer.mozilla.org/docs/Web/API/GlobalFetch/fetch) method, so that you can no longer use those names for your global variables. *Dailymotion* is known to be affected by this change, because the site had its own `Request` object.

Firefox 39 has also implemented and enabled the [Service Worker](https://developer.mozilla.org/docs/Web/API/ServiceWorker_API) Cache API on the Aurora and Nightly channels, so you may have to be careful with the new [`Cache`](https://developer.mozilla.org/docs/Web/API/Cache) and [`CacheStorage`](https://developer.mozilla.org/docs/Web/API/CacheStorage) interfaces as well.
