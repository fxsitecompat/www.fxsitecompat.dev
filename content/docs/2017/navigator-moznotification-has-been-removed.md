---
title: "`navigator.mozNotification` has been removed"
date: "2017-12-09T00:36:00-05:00"
categories: ["dom"]
tags: []
versions: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=952453"
      title: "Bug 952453 - Remove mozNotification (DesktopNotification) API"
aliases:
    - "/en-CA/docs/2015/navigator-moznotification-will-be-removed/"
---
The non-standard [`navigator.mozNotification`](https://developer.mozilla.org/docs/Web/API/Navigator/mozNotification) object, available only on Firefox for Android and deprecated since Firefox 22, has been removed with Firefox 59. Use the standard [Notifications API](https://developer.mozilla.org/docs/Web/API/Notifications_API) instead.
