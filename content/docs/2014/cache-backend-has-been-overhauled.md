---
title: "Cache backend has been overhauled"
date: "2014-06-09T02:46:54-04:00"
categories: ["networking"]
tags: []
versions: ["32", "38-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=913806"
      title: "Bug 913806 – Turn HTTP cache v2 on by default on all products"
---
The new HTTP cache backend has been landed on Firefox 32 to improve the page load performance. See [Honza Bambas' blog post](https://www.janbambas.cz/new-firefox-http-cache-enabled/) for details. If you encountered any regressions, please [report the issue](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Networking%3A%20Cache) to Bugzilla.
