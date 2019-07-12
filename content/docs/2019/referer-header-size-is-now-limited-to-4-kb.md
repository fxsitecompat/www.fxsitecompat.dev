---
title: "`Referer` header size is now limited to 4 KB"
date: "2019-07-11T23:03:00-04:00"
categories: ["networking"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1557346"
      title: "Bug 1557346 - Experiment limit `referer` header length"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/GWvDmAn8n3M/discussion"
      title: "Intent to implement and ship: Limit the length of Referer header to 4k"
---
Starting with Firefox 70, the size of the `Referer` HTTP request header is limited to 4 KB (4,096 bytes). If an overly long referer exceeds the defined limit, only the origin part will be sent. If the origin part still exceeds the limit, which is unlikely to happen though, the header will be completely truncated.

[Google Chrome](https://www.chromestatus.com/feature/5648956820291584) has made the same change in version 77.
