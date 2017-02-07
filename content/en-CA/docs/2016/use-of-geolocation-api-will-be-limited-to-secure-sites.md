---
title: "Use of Geolocation API will be limited to secure sites"
date: "2016-04-26T22:17:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
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
    - "/docs/2016/use-of-geolocation-watchposition-will-be-limited-to-secure-sites/"
---
As part of the [insecure HTTP deprecation](https://www.fxsitecompat.com/en-CA/docs/2015/insecure-http-will-be-deprecated/), the [Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation) will soon be available only to sites using a secure connection. [Chrome 50](https://developers.google.com/web/updates/2016/04/geolocation-on-secure-contexts-only) has already introduced this limitation.

**Update**: Updated this document as Mozilla developers have decided to disable not only [`watchPosition`](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/watchPosition) but also the [`getCurrentPosition`](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/getCurrentPosition) method on non-secure sites.

**Update 2**: This change is currently planned for Firefox 55 coming August 2017.
