---
title: "`MouseEvent.mozPressure` will be removed"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165211"
      title: "Bug 1165211 - Remove MouseEvent.mozPressure."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=822898"
      title: "Bug 822898 - Implement pointer events"
---
The `MouseEvent.mozPressure` property will be removed in favour of the standard `PointerEvent.pressure` property. The [Pointer Events API](https://www.w3.org/TR/pointerevents/) is currently being implemented.
