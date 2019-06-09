---
title: "`setTimeout()`/`setInterval()` are now deferred during page load"
date: "2019-02-18T17:08:00-05:00"
categories: ["misc"]
tags: []
versions: ["66"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270059"
      title: "Bug 1270059 - make setTimeout() low priority during page load"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1524952"
      title: "Bug 1524952 - Low-priority setTimeout() breaks slider on bestbuy.com"
---
Starting with Firefox 66, timers added with the `window.setTimeout` or `window.setInterval` method during page load will be given a low priority and deferred until an idle time is available or the loading is complete.

While this change aims at improving the performance of complex web applications like *Google Docs*, unexpected race conditions could occur if the initialization code is not designed properly. One regression on the *Best Buy*'s website has been reported and later fixed by themselves, which was likely due to a change in the resource access order, according to a Mozilla developer.

Remember that timers on the web are not so accurate. [It may take longer than specified](https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/setTimeout#Reasons_for_delays_longer_than_specified) for various reasons, such as when the browser tab is in background.

**Update**: [Firefox 68](https://www.fxsitecompat.com/en-CA/docs/2019/xhr-load-loadend-events-are-now-deferred-during-page-load/) has made a similar change to XHR final events.
