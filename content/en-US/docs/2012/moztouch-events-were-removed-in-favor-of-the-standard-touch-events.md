---
title: "`MozTouch` events were removed in favor of the standard touch events"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: "18"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=726615": "Bug 726615 – Support W3C touch event instead of MozTouch event"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=798821": "Bug 798821 – Disable touch events on Windows for devices that do not support touch input"
---
The experimental, deprecated [`MozTouch*` API](https://developer.mozilla.org/en-US/docs/Web/Guide/DOM/Events/Touch_events_%28Mozilla_experimental%29) (the `MozTouchDown`, `MozTouchMove`, `MozTouchUp` events) has been removed. The [W3C standard touch events](https://developer.mozilla.org/en-US/docs/Web/Guide/DOM/Events/Touch_events) should be used instead.

To maintain site compatibility, on Windows, Firefox detects whether touch input is supported and disables touch events on incompatible computers. According to a comment in the bug, compatible computers are only a few percent for now. On Android, touch events are enabled by default. On Mac and Linux, touch events are not implemented yet.

**[Compatibility issues with touch events](https://bugzilla.mozilla.org/showdependencytree.cgi?id=806805&hide_resolved=1) have been found on many sites**. If your site or application has supported touch events for mobile, please test with desktop browsers including Firefox to ensure it works as expected.
