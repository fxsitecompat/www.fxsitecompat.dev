---
title: "Vibration API can no longer be used from cross-origin `<iframe>`"
date: "2019-11-13T14:44:00-05:00"
categories: ["dom"]
tags: []
releases: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1591113"
      title: "Bug 1591113 - Remove support for third-party vibrate"
---
Using the [Vibration API](https://developer.mozilla.org/docs/Web/API/Vibration_API) in a cross-origin `<iframe>` is no longer allowed on Firefox 72 and later, because the API is sometimes abused by untrusted third parties. From now on, calling the `navigator.vibrate` method will silently fail in such cases. Google Chrome has already made the [same change](https://www.chromestatus.com/feature/5682658461876224) in version 55.
