---
title: "`navigator.registerProtocolHandler()` can no longer be used on insecure sites"
date: "2018-05-11T14:47:00-04:00"
categories: ["html", "privacy-security"]
tags: []
releases: ["62", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460506"
      title: "Bug 1460506 - registerProtocolHandler require SecureContext in stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zzBWOPMPPs0/discussion"
      title: "Intent to Unship: registerProtocolHandler() over insecure contexts"
aliases:
    - "/en-CA/docs/2018/registerprotocolhandler-can-no-longer-be-used-on-insecure-sites/"
---
Starting with Firefox 62, the [`navigator.registerProtocolHandler`](https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler) method will be `undefined` on non-HTTPS sites, preventing insecure applications from being registered for the browser as a protocol handler. This security restriction has already been introduced to Firefox Nightly and early Beta/DevEdition since the [version 60](https://www.fxsitecompat.dev/en-CA/docs/2018/support-for-registerprotocolhandler-on-insecure-sites-has-been-deprecated/).
