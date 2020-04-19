---
title: "`fetch()` and `Request` now throws if redirect is detected when in non-`follow` redirect mode"
date: "2016-05-10T20:30:00-04:00"
categories: ["dom"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1243792"
      title: "Bug 1243792 - add fetch Response.redirected and additional security restrictions"
---
In order to avoid the risk of open redirectors, the [`fetch`](https://developer.mozilla.org/docs/Web/API/GlobalFetch/fetch) method and the [`Request`](https://developer.mozilla.org/docs/Web/API/Request/Request) constructor now raises a network error when a request's `redirect` option is set to `manual` or `error` and the response contains one or more redirects. Also, the `redirected` property has been added the [`Response`](https://developer.mozilla.org/docs/Web/API/Response) interface so that developers can check this new property to avoid untrustworthy responses.
