---
title: "TLS 1.0/1.1 support has been removed"
date: "2020-01-08T19:23:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1606734"
      title: "Bug 1606734 - Disable TLS 1.0 and 1.1 by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8EFRYDR3N1c/discussion"
      title: "Intent to unship: TLS 1.0 and TLS 1.1"
    - url: "https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/"
      title: "TLS 1.0 and 1.1 Removal Update - Mozilla Hacks"
---
The support for the [Transport Layer Security](https://developer.mozilla.org/docs/Web/Security/Transport_Layer_Security) (TLS) protocol's version 1.0 and 1.1, deprecated since [Firefox 71](https://www.fxsitecompat.dev/en-CA/docs/2019/tls-1-0-and-1-1-are-now-deprecated-disabled-in-nightly/), has been removed from all the channels as of Firefox 74. All major browsers are going to drop the support for the older versions of TLS in early 2020.

Make sure to enable TLS 1.2 or 1.3 on your web server, otherwise Firefox will show the [Secure Connection Failed](https://support.mozilla.org/kb/secure-connection-failed-firefox-did-not-connect) error page to prevent users from accessing servers not using the newer version. See [this Mozilla Hacks blog post](https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/) for more information.
