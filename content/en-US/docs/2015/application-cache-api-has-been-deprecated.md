---
title: "Application Cache API has been deprecated"
date: "2015-09-25T01:55:00-04:00"
categories: ["html"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1204581": "Bug 1204581 - Add a deprecation notice for AppCache if service worker fetch interception is enabled"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1163545": "Bug 1163545 - Bypass AppCache completely when Service Workers supported & registered"
---
The HTML5 [Application Cache API](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache) (AppCache), that enables [offline support](https://developer.mozilla.org/en-US/Apps/Build/Offline) in Web applications, is now considered deprecated and will be [removed from a future Firefox release](https://www.fxsitecompat.com/en-US/docs/2016/application-cache-support-will-be-removed/). Web developers are encouraged to learn [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) as an alternative solution, so that you can offer a richer, more seamless offline user experience sometime soon. This new API is already available on [Firefox Developer Edition](https://www.mozilla.org/firefox/developer/) for testing, though not all the features are implemented yet. Note that AppCache is ignored when a Service Worker is registered.
