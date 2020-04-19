---
title: "Legacy Proxy API has been removed"
date: "2016-03-12T18:44:00-05:00"
categories: ["javascript"]
tags: []
releases: ["48", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=892903"
      title: "Bug 892903 - Remove Proxy.create and Proxy.createFunction"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244442"
      title: "Bug 1244442 - Warn about Proxy.create and Proxy.createFunction"
aliases:
    - "/en-CA/docs/2015/legacy-proxy-api-will-be-removed/"
---
The non-standard, [legacy Proxy API](https://developer.mozilla.org/docs/Archive/Web/Old_Proxy_API), including the `Proxy.create` and `Proxy.createFunction` methods [deprecated since Firefox 18](https://www.fxsitecompat.dev/en-CA/docs/2012/proxy-api-has-been-updated-for-the-new-spec/), has been removed with Firefox 48. The Web Console shows the deprecation warning on Firefox 47. Use the [standardized Proxy API](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) instead.
