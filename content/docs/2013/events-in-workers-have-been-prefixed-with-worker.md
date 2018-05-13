---
title: "Events in workers have been prefixed with `Worker`"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=887236"
      title: "Bug 887236 – prefix the current events in workers with \"Worker\""
---
In order to make [normal DOM events](https://developer.mozilla.org/docs/Web/Reference/Events) work in [Web workers](https://developer.mozilla.org/docs/Web/Guide/Performance/Using_web_workers), the current events in workers including [`Event`](https://developer.mozilla.org/docs/Web/API/Event), [`MessageEvent`](https://developer.mozilla.org/docs/Web/API/MessageEvent), [`ErrorEvent`](https://developer.mozilla.org/docs/Web/API/ErrorEvent) and [`ProgressEvent`](https://developer.mozilla.org/docs/Web/API/ProgressEvent) have been renamed to `WorkerEvent`, `WorkerMessageEvent`, `WorkerErrorEvent` and `WorkerProgressEvent`. This change is **temporary**. Once the Firefox back-end implementation is fixed, those events will be unprefixed again.
