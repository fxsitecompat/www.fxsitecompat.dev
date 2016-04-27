---
title: "Use of `Geolocation.watchPosition()` will be limited to secure sites"
date: "2016-04-26T22:17:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Deprecate non-TLS usage of geolocation"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1266494"
      title: "Bug 1266494 - Limit navigator.geolocation.watchPosition() to secure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wouDQLBbm9A/discussion"
      title: "Intent to ship: Restrict geolocation.watchPosition to secure contexts"
---
As part of the [insecure HTTP deprecation](https://www.fxsitecompat.com/en-CA/docs/2015/insecure-http-will-be-deprecated/), the [Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation) will be available only to sites using a secure connection. Chrome 50 has already introduced this limitation. Mozilla developers are also considering preventing the [`watchPosition`](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/watchPosition) method from being used by non-secure sites in Firefox, given that it's a "powerful" feature with less usage than the [`getCurrentPosition`](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/getCurrentPosition) method.
