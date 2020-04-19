---
title: "`Proxy-Connection` header has gone"
date: "2012-12-03T03:53:26-05:00"
categories: ["networking"]
tags: []
releases: ["18", "24-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=570283"
      title: "Bug 570283 – Stop sending Proxy-Connection"
---
The `Proxy-Connection` request header, that has been sent when HTTP proxy is enabled, has been removed. This header was non-standard and hasn't worked properly.
