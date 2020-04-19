---
title: "Workers will no longer dispatch `close` event"
date: "2016-09-02T03:32:00-04:00"
categories: ["dom"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=790919"
      title: "Bug 790919 - Don't dispatch close event, and remove onclose"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/mqKBGePe4-s/discussion"
      title: "Intent to unship: WorkerGlobalScope.onclose"
---
The [`WorkerGlobalScope.onclose`](https://developer.mozilla.org/docs/Web/API/WorkerGlobalScope/onclose) property has been removed because it was dropped from the spec a long time ago, and therefore Web workers will no longer dispatch the [`close`](https://developer.mozilla.org/docs/Web/Events/close) event. Since no other browsers implement it, the compatibility impact should be minimum.
