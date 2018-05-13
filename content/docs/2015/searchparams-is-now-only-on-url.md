---
title: "`searchParams` is now only on `URL`"
date: "2015-11-28T19:24:00-08:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1213815"
      title: "Bug 1213815 - searchParams is just on URL"
---
The [`URLUtils`](https://developer.mozilla.org/docs/Web/API/URLUtils) interface has been removed, and the [`searchParams`](https://developer.mozilla.org/docs/Web/API/URLUtils/searchParams) property is no longer available on the [`Location`](https://developer.mozilla.org/docs/Web/API/Location), [`WorkerLocation`](https://developer.mozilla.org/docs/Web/API/WorkerLocation), [`HTMLAnchorElement`](https://developer.mozilla.org/docs/Web/API/HTMLAnchorElement) and [`HTMLAreaElement`](https://developer.mozilla.org/docs/Web/API/HTMLAreaElement) interfaces. That means the property is only available on the [`URL`](https://developer.mozilla.org/docs/Web/API/URL) interface from now on.
