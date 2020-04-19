---
title: "XHR `load`, `loadend`, `readystatechange` events are now deferred during page load"
date: "2019-06-09T03:18:00-04:00"
categories: ["dom", "networking"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1538364"
      title: "Bug 1538364 - Consider firing the load/loadend/final readyState events for XHR later during page load (after page load event if possible)"
---
Starting with Firefox 68, final events for `XMLHttpRequest` started during page load will be deferred until an idle time is available or the loading is complete. These events include `load`, `loadend` and `readystatechange` fired once the `readyState` property becomes `4`.

Just like a similar change made to `setTimeout()` with [Firefox 66](https://www.fxsitecompat.dev/en-CA/docs/2019/settimeout-and-setinterval-are-now-deferred-during-page-load/), this change aims at improving the performance of complex web applications like *Gmail*, but unexpected race conditions could occur if the initialization code is not designed properly.

**Update**: [Firefox 69](https://www.fxsitecompat.dev/en-CA/docs/2019/resolving-promise-returned-by-fetch-is-now-deferred-during-page-load/) has made a similar change to `fetch()` as well.
