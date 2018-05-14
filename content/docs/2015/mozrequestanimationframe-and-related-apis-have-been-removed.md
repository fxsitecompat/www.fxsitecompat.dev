---
title: "`mozRequestAnimationFrame` and related APIs have been removed"
date: "2015-08-05T00:48:18-04:00"
categories: ["dom"]
tags: []
versions: ["42"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909154"
      title: "Bug 909154 - Consider removing support for the prefixed mozRequestAnimationFrame"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/nULjUn_Zg1w/discussion"
      title: "Intent to unship: Prefixed mozRequestAnimationFrame and related APIs (mozAnimationStartTime, mozCancelAnimationFrame)"
---
The `mozRequestAnimationFrame`, `mozCancelAnimationFrame` and `mozCancelRequestAnimationFrame` methods, [deprecated since Firefox 23](https://www.fxsitecompat.com/en-CA/docs/2013/requestanimationframe-and-cancelanimationframe-have-been-unprefixed/), have been removed in favour of the standard [`requestAnimationFrame`](https://developer.mozilla.org/docs/Web/API/Window/requestAnimationFrame) and [`cancelAnimationFrame`](https://developer.mozilla.org/docs/Web/API/Window/cancelAnimationFrame) methods. The [`mozAnimationStartTime`](https://developer.mozilla.org/docs/Web/API/Window/mozAnimationStartTime) property has also been removed but the compatibility impact should be minimum since no other browsers implement the equivalent.
