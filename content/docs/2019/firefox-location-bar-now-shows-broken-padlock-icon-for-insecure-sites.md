---
title: "Firefox location bar now shows broken padlock icon for insecure sites"
date: "2019-07-21T21:13:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1562881"
      title: "Bug 1562881 - [Protections Panel] Remove \"i\" icon and make the shield icon persistent on the URL bar."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RzmOHmoksdU/discussion"
      title: "Intent to Ship: Show an indicator for insecure HTTP in the URL bar"
    - url: "https://blog.mozilla.org/security/2019/10/15/improved-security-and-privacy-indicators-in-firefox-70/"
      title: "Mozilla Security Blog: Improved Security and Privacy Indicators in Firefox 70"
---
As part of the ongoing [insecure HTTP deprecation](https://www.fxsitecompat.dev/en-CA/docs/2015/insecure-http-will-be-deprecated/), Firefox 70 starts showing a broken padlock icon in the location bar whenever the user visits an insecure site, similarly to [Google Chrome](https://www.blog.google/products/chrome/milestone-chrome-security-marking-http-not-secure/) and [Safari](https://support.apple.com/en-us/HT208672) already showing a "not secure" label.

<img src="/images/screenshots/1562881-insecure-icon.png" width="160" height="80" alt="">

This actually doesn't affect anything about site compatibility, but for better security and user experience, webmasters are strongly encouraged to serve their site via HTTPS.
