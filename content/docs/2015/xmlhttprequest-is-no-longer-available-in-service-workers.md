---
title: "`XMLHttpRequest` is no longer available in Service Workers"
date: "2015-10-23T01:34:00-07:00"
categories: ["dom"]
tags: []
releases: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=931243"
      title: "Bug 931243 - XMLHttpRequest should be disabled on ServiceWorkers"
---
The [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) API has been disabled in [Service Workers](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) as per the latest spec. Use the [Fetch API](https://developer.mozilla.org/docs/Web/API/Fetch_API) instead. The Service Worker API is currently enabled only on the [Developer Edition](https://www.mozilla.org/firefox/developer/) (Aurora) and Nightly channels, so the compatibility impact should be minimum.

**Update**: The Service Worker API has been shipped with Firefox 44, so it's now available on the Beta and Release channels as well.
