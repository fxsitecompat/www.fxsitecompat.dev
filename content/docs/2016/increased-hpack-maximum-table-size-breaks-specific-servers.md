---
title: "Increased HPACK maximum table size breaks specific servers"
date: "2016-10-07T00:55:00-04:00"
categories: ["networking"]
tags: []
versions: ["52", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1296280"
      title: "Bug 1296280 - Change HPACK receive table size to 64k"
---
Firefox 52 for desktop has changed the maximum table size of HPACK, an HTTP/2 header compression format, from 4 KB to 64 KB. There are certain types of Web server software that cannot handle this new configuration properly.

According to bug reports, *Apache Tomcat* has fixed the issue with the version 8.5.6 and 9.0.0.M11. The *Node.js SPDY Server* module 3.3.x also has the bug but the version 3.4.x doesn't. If you're using one of these servers, upgrade to the latest available version to avoid the interoperability issue.
