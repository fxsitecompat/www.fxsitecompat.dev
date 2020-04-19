---
title: "Notifications API can no longer be used on insecure sites"
date: "2019-05-13T01:47:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
releases: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1429432"
      title: "Bug 1429432 - Consider making Notifications require SecureContext"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FMPrIMGBNtg/discussion"
      title: "Intent to require Secure Context for Web Notifications"
---
As of Firefox 67, the Notifications API requires sites to be served via HTTPS in order to request a permission to display desktop notifications, including push notifications through a service worker. Since the Service Worker API and Push API have always required secure sites, this change only affects traditional use cases of the `Notification.requestPermission` method, which is currently less than 2% according to Mozilla's Telemetry. The console logs an error when a request is forbidden. [Google Chrome](https://www.chromestatus.com/feature/5759967025954816) has already done the same change in 62.
