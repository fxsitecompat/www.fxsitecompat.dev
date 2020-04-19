---
title: "Use of Geolocation API is now limited to secure sites"
date: "2017-03-09T14:18:00-05:00"
categories: ["misc", "privacy-security"]
tags: []
releases: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Disable Geolocation on non-secure origins"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wouDQLBbm9A/discussion"
      title: "Intent to ship: Restrict geolocation.watchPosition to secure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/BvcsTpAqIsQ/discussion"
      title: "Intent to restrict to secure contexts: navigator.geolocation"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8BsF76gNhDE/discussion"
      title: "Intent to deprecate: insecure Geo requests"
aliases:
    - "/en-CA/docs/2016/use-of-geolocation-watchposition-will-be-limited-to-secure-sites/"
    - "/en-CA/docs/2016/use-of-geolocation-api-will-be-limited-to-secure-sites/"
---
As part of the ongoing [insecure HTTP deprecation](https://www.fxsitecompat.dev/en-CA/docs/2015/insecure-http-will-be-deprecated/), the [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation), including the [`getCurrentPosition`](https://developer.mozilla.org/docs/Web/API/Geolocation/getCurrentPosition) and [`watchPosition`](https://developer.mozilla.org/docs/Web/API/Geolocation/watchPosition) methods, can now be used only on sites using a secure connection. Given that [Chrome 50](https://developers.google.com/web/updates/2016/04/geolocation-on-secure-contexts-only) has already introduced this limitation in April 2016, the compatibility risk is considered low at this moment. The solution is, obviously, moving your site to HTTPS.
