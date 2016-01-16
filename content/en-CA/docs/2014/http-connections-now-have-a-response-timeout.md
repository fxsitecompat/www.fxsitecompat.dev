---
title: "HTTP connections now have a response timeout"
date: "2014-02-07T11:57:09-05:00"
categories: ["networking"]
tags: []
versions: ["29"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=947391": "Bug 947391 – HTTP connections (exc. XHR, SPDY) should have a response timeout"
---
Firefox has enabled a timeout to drop HTTP connections, except XMLHttpRequest and SPDY sessions, if the response takes too long. The initial value is 300 seconds or 5 minutes. If your application is processing large data and affected by this change, you can change the value of the `network.http.response.timeout` preference to a larger number via [about:config](http://kb.mozillazine.org/About:config).
