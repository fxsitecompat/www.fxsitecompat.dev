---
title: "`Accept` header for XHR has been simplified"
date: "2016-09-07T02:26:00-04:00"
categories: ["networking"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=918752"
      title: "Bug 918752 - [XHR2] Default Accept: header more complex than */*"
---
Firefox was previously sending `text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8` as the `Accept` HTTP header's value for the [`XMLHttpRequest.send`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/send) method when no developer-defined value is given with the [`setRequestHeader`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/setRequestHeader) method. The default value will be `*/*` on Firefox 51 and later according to the XMLHttpRequest Level 2 spec.
