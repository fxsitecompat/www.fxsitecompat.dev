---
title: "Application Cache storage has been removed"
date: "2020-04-17T08:01:00-04:00"
categories: ["html"]
tags: []
versions: ["77"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782"
      title: "Bug 1237782 - Remove support for appcache storage in Nightly and early beta"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1619673"
      title: "Bug 1619673 - Disable appcache in release"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5JqnS_PnKqU/discussion"
      title: "Intent to unship AppCache"
aliases:
    - "/en-CA/docs/2016/application-cache-support-will-be-removed/"
    - "/en-CA/docs/2019/application-cache-storage-has-been-removed-in-nightly-and-early-beta/"
---
The browser storage for [HTML Application Cache](https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache) (AppCache), deprecated since [Firefox 44](https://www.fxsitecompat.dev/en-CA/docs/2015/application-cache-api-has-been-deprecated/) and already removed from the Nightly and early Beta channels since Firefox 71, is no longer available in all channels as of Firefox 77.

The `applicationCache` property and `OfflineResourceList` interface are still exposed on `window` to avoid possible site breakage, but the now-useless DOM API will also be removed in the near future. Use the [Service Workers API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) to offer a [richer offline experience](https://serviceworke.rs/).

Google is also removing the AppCache storage with [Chrome 84](https://bugs.chromium.org/p/chromium/issues/detail?id=582750#c47).
