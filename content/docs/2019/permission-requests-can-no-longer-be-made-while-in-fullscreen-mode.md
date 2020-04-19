---
title: "Permission requests can no longer be made while in fullscreen mode"
date: "2019-09-05T06:42:00-04:00"
categories: ["misc"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1412561"
      title: "Bug 1412561 - Add-on installation should be blocked when in full-screen mode"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1522120"
      title: "Bug 1522120 - Exit fullscreen when a permission prompt is shown to the user"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1577478"
      title: "Bug 1577478 - Log warning to website console when permission prompt / full-screen is cancelled"
---
There are various known sites that trap users in the browser's [fullscreen mode](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) and force them to accept a [permission request](https://developer.mozilla.org/docs/Web/API/Permissions_API), which allows the site to send annoying push notifications, access the computer's camera and mic, or even install a malicious extension to the browser. In order to mitigate these risks, Firefox 70 has made the following changes:

* Cancel any pending permission request when entering fullscreen mode
* Exit fullscreen when a permission request is made while in fullscreen mode
* Block add-on installations while in fullscreen mode (since Firefox 68)

It means, if you're using the Fullscreen API for a custom video player, an immersive game or whatever, you need to make necessary permission requests before entering fullscreen mode, otherwise the user experience could be degraded.

To better inform developers, Firefox 71 and later will log a warning in the web console when a permission request or fullscreen mode is cancelled.
