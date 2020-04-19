---
title: "Support for `registerProtocolHandler()` on insecure sites has been deprecated"
date: "2018-02-11T00:01:00-05:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1429732"
      title: "Bug 1429732 - Consider making registerProtocolHandler require SecureContext"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zzBWOPMPPs0/discussion"
      title: "Intent to Unship: registerProtocolHandler() over insecure contexts"
---
As part of the ongoing [insecure HTTP deprecation](https://www.fxsitecompat.dev/en-CA/docs/2015/insecure-http-will-be-deprecated/), Firefox 60 Nightly will no longer allow non-HTTPS sites to use the [`navigator.registerProtocolHandler`](https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler) method to register itself as a protocol handler, e.g. `mailto` for a webmail service. Given the low usage rate of the functionality, Firefox 62 will make the change on all the channels according to the current plan.

**Update**: As planned, all the channels impose the restriction as of [Firefox 62](https://www.fxsitecompat.dev/en-CA/docs/2018/registerprotocolhandler-can-no-longer-be-used-on-insecure-sites/).
