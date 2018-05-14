---
title: "Quality factor in request headers can now have 2 decimal places"
date: "2012-12-03T03:53:26-05:00"
categories: ["networking"]
tags: []
versions: ["18"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672448"
      title: "Bug 672448 – Clamp quality factor (\'q\') values to 2 decimal places"
---
Previously Firefox has been clamped the quality factors to one decimal place. The quality factors are numerical values following `q=`, specified in HTTP request headers like [`Accept-Language`](https://developer.mozilla.org/docs/HTTP/Content_negotiation#The_Accept-Language.3A_header). With such implementation, multiple items may have the same value, thus it has been changed to reflect 2 decimal places to make those values explicit.
