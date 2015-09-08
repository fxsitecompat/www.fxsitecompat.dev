---
title: "`MouseEvent.offsetX`/`Y` has been implemented; Google Maps API behaves wrongly"
date: "2015-07-13T10:05:10-04:00"
categories: ["dom"]
tags: ["regression"]
versions: "39"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=69787": "Bug 69787 - Implement MSIE\'s event.offsetX, event.offsetY as mouse coordinates inside target element"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1175863": "Bug 1175863 - Google Maps API V3 drawing manager bug"
    "https://groups.google.com/d/topic/mozilla.dev.platform/ibv6l2-LG3E/discussion": "Intent to ship: MouseEvent.offsetX/Y"
---
The MSIE-derived [`MouseEvent.offsetX`](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/offsetX) and [`MouseEvent.offsetY`](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/offsetY) properties have been standardized in the CSSOM View specification and now implemented in Firefox. This change exposes a [bug in the Google Maps API's Drawing Layer](https://code.google.com/p/gmaps-api-issues/issues/detail?id=8278) where incorrect mouse coordinates are returned likely due to a poor user-agent detection. Google is working on the fix.

**Update**: Google has not deployed the fix, but according to a [comment](https://bugzilla.mozilla.org/show_bug.cgi?id=1175863#c24) in the bug, it is possible to workaround the issue by adding `v=3` to the Maps API script URL.
