---
title: "`progress` events will no longer be fired for sync XHR in workers"
date: "2018-09-06T01:36:00-04:00"
categories: ["dom"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1459984"
      title: "Bug 1459984 - Avoid firing an event named progress with synchronous XMLHttpRequest"
---
Starting with Firefox 63, the [`progress`](https://developer.mozilla.org/docs/Web/Events/progress) events will no longer be fired for synchronous requests within workers, according to the latest `XMLHttpRequest` spec. On the main thread, this type of event hasn't been fired at least since Firefox 52. If you'd like to [monitor progress](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest#Monitoring_progress) on download or upload, you have to use an asynchronous request which is not affected by this change.
