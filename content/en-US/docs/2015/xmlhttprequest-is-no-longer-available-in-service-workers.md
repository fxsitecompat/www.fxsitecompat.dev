---
title: "`XMLHttpRequest` is no longer available in Service Workers"
date: "2015-10-23T01:34:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=931243": "Bug 931243 - XMLHttpRequest should be disabled on ServiceWorkers"
---
The [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) API has been disabled in [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) as per the latest spec. The Service Worker API is currently enabled only on the [Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) (Aurora) and Nightly channels, so the compatibility impact should be minimum.
