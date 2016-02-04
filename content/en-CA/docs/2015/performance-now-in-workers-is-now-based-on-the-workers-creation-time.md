---
title: "`performance.now` in workers is now based on the worker's creation time"
date: "2015-12-17T14:39:00-05:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "reverted"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1169068": "Bug 1169068 - Update the High Resolution Time API to the latest version of the spec"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1226147": "Bug 1226147 - WorkerPrivate->NowBaseTimeStamp() should not return the parent->GetPerformance()->Now() in dedicated Workers."
    "https://groups.google.com/d/topic/mozilla.dev.platform/PBiil3ItyeY/discussion": "Intent to implement and ship: Changes to Worker performance.now() zero time"
---
Starting with Firefox 45, the [`performance.now`](https://developer.mozilla.org/en-US/docs/Web/API/Performance/now) method in workers will return a [`DOMHighResTimeStamp`](https://developer.mozilla.org/en-US/docs/Web/API/DOMHighResTimeStamp) from the worker's creation time instead of the [navigation start time](https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming/navigationStart) inherited from the parent window or worker, as per the latest High Resolution Time spec. The new [`Performance.translateTime`](https://w3c.github.io/hr-time/#dom-performance-translatetime) method can be used to get a timestamp based on the main window context as before.

**Update**: This change has been [reverted](https://bugzilla.mozilla.org/show_bug.cgi?id=1243881) during the Firefox 45 Beta cycle because the spec seems unstable yet.
