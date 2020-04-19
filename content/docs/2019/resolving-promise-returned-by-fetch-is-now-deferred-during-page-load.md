---
title: "Resolving `Promise` returned by `fetch()` is now deferred during page load"
date: "2019-06-15T21:58:00-04:00"
categories: ["dom", "networking"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1538516"
      title: "Bug 1538516 - Resolve the Promise returned by fetch() later during page loads"
---
Starting with Firefox 69, a `Promise` returned by `fetch()` during page load won't be resolved until an idle time is available or the loading is complete. This change aims at improving page load performance, just like similar changes recently made to [`setTimeout()`](https://www.fxsitecompat.dev/en-CA/docs/2019/settimeout-and-setinterval-are-now-deferred-during-page-load/) and [`XMLHttpRequest`](https://www.fxsitecompat.dev/en-CA/docs/2019/xhr-load-loadend-readystatechange-events-are-now-deferred-during-page-load/), but unexpected race conditions may occur if the initialization code is not designed properly. Make sure to test your site if applicable.
