---
title: "TLS 1.0 and 1.1 are now deprecated, disabled in Nightly"
date: "2019-09-27T22:53:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1579270"
      title: "Bug 1579270 - Disable TLS 1.0 and 1.1 for Nightly"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8EFRYDR3N1c/discussion"
      title: "Intent to unship: TLS 1.0 and TLS 1.1"
    - url: "https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/"
      title: "TLS 1.0 and 1.1 Removal Update - Mozilla Hacks"
aliases:
    - "/en-CA/docs/2019/tls-1-0-and-1-1-are-now-deprecated/"
---
The support for [Transport Layer Security](https://developer.mozilla.org/docs/Web/Security/Transport_Layer_Security) (TLS) 1.0 and 1.1 has been deprecated and will be removed from all major browsers in March 2020. The older versions of TLS are now disabled by default in Firefox Nightly in preparation for the removal, which means the browser shows the [Secure Connection Failed](https://support.mozilla.org/kb/secure-connection-failed-firefox-did-not-connect) error page to prevent access to web servers not using TLS 1.2 or 1.3.

Make sure to enable the newer versions of TLS on your server so it remains safe and available. See [this Mozilla Hacks blog post](https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/) for more information.
