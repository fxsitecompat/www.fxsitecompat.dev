---
title: "Notification permission requests from cross-origin `<iframe>` are now disallowed"
date: "2019-08-13T14:24:00-04:00"
categories: ["dom"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1560741"
      title: "Bug 1560741 - Disallow notification permission requests from cross-origin iframes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/-6HYtlHuYO8/discussion"
      title: "Intent to ship: restrict access to request notification permissions from cross-origin iframes"
---
Starting with Firefox 70, requests for the desktop notification permission will all be denied when the `Notification.requestPermission` method is called from a cross-origin `<iframe>`. Once blocked, no prompt will be displayed and web console logs a warning. According to Mozilla's Telemetry, such permission requests are less than 0.03%, so the compatibility risk should be very low.

In the future, requests from a same-origin `<iframe>` may also be denied. If you need a permission, make sure to request it from a top-level document.
