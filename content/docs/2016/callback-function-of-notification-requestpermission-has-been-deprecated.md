---
title: "Callback function of `Notification.requestPermission()` has been deprecated"
date: "2016-03-10T07:04:00-05:00"
categories: ["dom"]
tags: []
versions: ["46", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1241278"
      title: "Bug 1241278 - `Notification.requestPermission()` should return a promise"
---
The support for the [`Notification.requestPermission`](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method has been updated for the latest Notifications API spec. The method now returns a `Promise` that resolves to a permission value, and the optional callback function is considered deprecated.
