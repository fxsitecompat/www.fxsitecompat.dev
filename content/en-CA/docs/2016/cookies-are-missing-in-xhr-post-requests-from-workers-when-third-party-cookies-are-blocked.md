---
title: "Cookies are missing in XHR POST requests from workers when third-party cookies are blocked"
date: "2016-03-23T17:59:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257861"
      title: "Bug 1257861 - Firefox 45 fails to send Cookie header with XHR post requests done from a web worker when third-party cookies are blocked"
---
Firefox 45 has introduced a regression where [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) POST requests made in [workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers) do not send the HTTP `Cookie` header, when the browser is configured to block third-party cookies and even if those resources are on the [same origin](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy). This seems related to [another third-party cookie issue](https://www.fxsitecompat.com/en-CA/docs/2016/some-sites-are-broken-when-third-party-cookies-are-blocked/) fixed with Firefox 45.0.1. Mozilla developers are working on the solution.
