---
title: "NPN support has been removed"
date: "2017-02-06T19:16:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1248198"
      title: "Bug 1248198 - Drop NPN support"
---
Firefox 53 has removed the support for Next Protocol Negotiation (NPN) in favour of [Application-Layer Protocol Negotiation](https://en.wikipedia.org/wiki/Application-Layer_Protocol_Negotiation) (ALPN). Since [Chrome 51](https://developers.google.com/web/updates/2016/04/chrome-51-deprecations) shipped in May 2016 has already made the same change, the compatibility impact should be minimum.
