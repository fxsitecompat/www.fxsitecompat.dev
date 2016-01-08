---
title: "Application Cache support will be removed"
date: "2016-01-08T00:06:00-05:00"
categories: ["html"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782": "Bug 1237782 - Remove support for appcache"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1163545": "Bug 1163545 - Bypass AppCache completely when Service Workers supported & registered"
---
The support for the [Application Cache API](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache) (AppCache), [deprecated since Firefox 44](https://www.fxsitecompat.com/en-US/docs/2015/application-cache-api-has-been-deprecated/), will be removed in the future in favor of the [Service Workers API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) that enables richer offline experience. AppCache can still be used as a fallback for legacy browsers, but will be ignored anyway when a Service Worker is registered.
