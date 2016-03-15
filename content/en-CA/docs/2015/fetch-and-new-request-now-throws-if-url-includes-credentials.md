---
title: "`fetch()` and `new Request()` now throws if URL includes credentials"
date: "2015-09-24T01:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1195820"
      title: "Bug 1195820 - fetch() and new Request() should throw TypeError on URL with username/password"
---
The Firefox implementation of the [`fetch`](https://developer.mozilla.org/en-US/docs/Web/API/GlobalFetch/fetch) method and [`Request`](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request) constructor was incorrectly accepting URLs containing a username and/or password, like `http://user:password@example.com`. Firefox 43 and later will throw a `TypeError` in such cases to comply with the Fetch API specification.
