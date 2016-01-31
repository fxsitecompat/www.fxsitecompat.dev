---
title: "Legacy Proxy API will be removed"
date: "2015-10-26T15:20:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=892903": "Bug 892903 - Remove Proxy.create and Proxy.createFunction"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1244442": "Bug 1244442 - Warn about Proxy.create and Proxy.createFunction"
---
The non-standard, [legacy Proxy API](https://developer.mozilla.org/en-US/docs/Archive/Web/Old_Proxy_API), including the `Proxy.create` and `Proxy.createFunction` methods [deprecated since Firefox 18](https://www.fxsitecompat.com/en-CA/docs/2012/proxy-api-has-been-updated-for-the-new-spec/), will be removed in the near future. The Web Console shows the deprecation warning on Firefox 47 and later. Use the [standardized Proxy API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) instead.
