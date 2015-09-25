---
title: "Application Cache API has been deprecated"
date: "2015-09-25T01:55:00-04:00"
categories: ["networking"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1204581": "Bug 1204581 - Add a deprecation notice for AppCache if service worker fetch interception is enabled"
---
The HTML5 [Application Cache API](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache) (AppCache), that enables [offline support](https://developer.mozilla.org/en-US/Apps/Build/Offline) in Web applications, is now considered deprecated and will be removed from a future Firefox release. The [Service Workers API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API), notably the methods on the [`Cache`](https://developer.mozilla.org/en-US/docs/Web/API/Cache) and [`CacheStorage`](https://developer.mozilla.org/en-US/docs/Web/API/CacheStorage) interfaces available since Firefox 41, can be used instead to offer a rich offline experience.
