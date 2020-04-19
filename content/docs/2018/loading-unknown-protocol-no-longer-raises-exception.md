---
title: "Loading unknown protocol no longer raises exception"
date: "2018-10-23T12:18:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=680300"
      title: "Bug 680300 - Restrict discoverability of protocol handlers [Tor 1623]"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/0KgeG3058NY/discussion"
      title: "Intent to implement: Suppress exception/error reporting when loading an unknown external protocol"
---
Previously, Firefox was raising the `NS_ERROR_UNKNOWN_PROTOCOL` exception when attempting to load an unknown external protocol with an image, frame or whatever. The following HTML code snippet posted to the bug shows an alert dialog depending on whether a specific browser extension is installed.

```html
<img src="sacore:green.gif"
     onerror="alert('McAfee Site Advisor not Installed.')"
     onload="alert('McAfee Site Advisor Installed!')">
```

Given that this could be a fingerprinting vector and other browsers don't report an error, Firefox 64 and later will no longer raise an exception to better protect user privacy.
