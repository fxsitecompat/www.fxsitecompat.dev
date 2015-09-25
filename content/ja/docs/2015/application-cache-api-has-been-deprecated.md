---
title: "Application Cache API が廃止予定となりました"
date: "2015-09-25T01:55:00-04:00"
categories: ["networking"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1204581": "Bug 1204581 - Add a deprecation notice for AppCache if service worker fetch interception is enabled"
---
Web アプリケーションの [オフライン対応](https://developer.mozilla.org/ja/Apps/Build/Offline) を可能にする HTML5 の [Application Cache API](https://developer.mozilla.org/ja/docs/Web/HTML/Using_the_application_cache) (AppCache) が廃止予定と見なされ、将来的に Firefox から削除されることとなりました。優れたオフライン体験を提供したい場合には、[Service Workers API](https://developer.mozilla.org/ja/docs/Web/API/Service_Worker_API)、特に Firefox 41 以降実装されている [`Cache`](https://developer.mozilla.org/ja/docs/Web/API/Cache)、[`CacheStorage`](https://developer.mozilla.org/ja/docs/Web/API/CacheStorage) 両インタフェース上のメソッドを代わりに使用してください。
