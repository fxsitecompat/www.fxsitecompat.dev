---
title: "`hasFeature()`/`isSupported()` methods now always return `true`"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
releases: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=801425"
      title: "Bug 801425 – Make hasFeature() and isSupported() always return true"
---
The [`document.implementation.hasFeature`](https://developer.mozilla.org/docs/Web/API/document.implementation.hasFeature) and [`Node.isSupported`](https://developer.mozilla.org/docs/Web/API/Node.isSupported) methods have been changed to always return `true`. The spec has been changed because those APIs were considered useless. However the SVG features are exception; those methods continue to return the support statuses.

**Update**: The SVG exception has been removed with [Firefox 51](https://www.fxsitecompat.dev/en-CA/docs/2016/hasfeature-will-always-return-true-even-for-svg/).
