---
title: "`event.timeStamp` now returns `DOMHighResTimeStamp` by default"
date: "2017-02-20T23:45:00-05:00"
categories: ["dom"]
tags: []
versions: ["54"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1026804"
      title: "Bug 1026804 - Make Event.timeStamp return a DOMHighResTimeStamp by default (switch on pref)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o1LT02foznI/discussion"
      title: "Intent to ship: Event.timeStamp as DOMHighResTimeStamp"
---
Starting with Firefox 54, on all Firefox channels and platforms, the [`Event.prototype.timeStamp`](https://developer.mozilla.org/en-US/docs/Web/API/Event/timeStamp) property will return a double [`DOMHighResTimeStamp`](https://developer.mozilla.org/en-US/docs/Web/API/DOMHighResTimeStamp) value since the [page load](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming/navigationStart), consisting of milliseconds in the integer part and microseconds in the decimal part, instead of an integer [`DOMTimeStamp`](https://developer.mozilla.org/en-US/docs/Web/API/DOMTimeStamp) value only in milliseconds since the epoch time.

This change has already been made on [Firefox Nightly and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) for [Windows](https://www.fxsitecompat.com/en-CA/docs/2014/event-timestamp-now-returns-domhighrestimestamp-on-nightly-aurora-for-windows/), [Linux](https://www.fxsitecompat.com/en-CA/docs/2015/event-timestamp-now-returns-domhighrestimestamp-on-nightly-aurora-for-linux/) and [macOS](https://bugzilla.mozilla.org/show_bug.cgi?id=1256562). As the [Android](https://bugzilla.mozilla.org/show_bug.cgi?id=1256565) implementation is now complete, the Beta and Release channels also enable high resolution timestamp by default.

Given that Google Chrome has enabled it since [Chrome 49](https://developers.google.com/web/updates/2016/01/high-res-timestamps) shipped in March 2016, the compatibility risk is considered low at this moment.
