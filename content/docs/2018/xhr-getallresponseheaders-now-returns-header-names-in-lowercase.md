---
title: "`XHR.getAllResponseHeaders()` now returns header names in lowercase"
date: "2018-09-27T15:18:00-04:00"
categories: ["dom"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398718"
      title: "Bug 1398718 - Remove default pref-off for lowercase header names in XHR.getAllResponseHeaders()"
---
Starting with Firefox 64, the [`XMLHttpRequest.getAllResponseHeaders`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/getAllResponseHeaders) method will return HTTP header names in lowercase letters, according to the current XMLHttpRequest spec. Mozilla once tried to make the change in Firefox 55, but it was reverted during the Nightly development cycle due to several compatibility issues. Now, given that [Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=716994) and [Safari](https://bugs.webkit.org/show_bug.cgi?id=169286) have already shipped the change, the compatibility risk should be low.
