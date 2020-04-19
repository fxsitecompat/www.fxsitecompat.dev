---
title: "`URL.createObjectURL()` is no longer available in service workers"
date: "2018-08-14T13:30:00-04:00"
categories: ["dom"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1264182"
      title: "Bug 1264182 - remove URL.createObjectURL from ServiceWorker"
---
The `URL.createObjectURL` and `URL.revokeObjectURL` static methods are now hidden from the service worker context, according to the latest Service Workers spec, due to `blob` URLs' lifecycle issues. These are still available in dedicated workers and shared workers as well as on `window`.
