---
title: "Cross-site `XMLHttpRequest` is blocked due to missing `Origin` header"
date: "2016-02-07T22:27:00-05:00"
categories: ["networking"]
tags: []
versions: ["43", "44"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1243453": "Bug 1243453 - Missing Origin header in Cross Origin Request resulting in Cross-Origin Request Blocked"
---
Firefox 43 introduced a regression regarding [cross-site `XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS) where the `Origin` header was missing in `GET` requests, resulting in an unnecessary preflight `OPTIONS` request and subsequent failed `GET` request. This bug has been fixed with Firefox 45.
