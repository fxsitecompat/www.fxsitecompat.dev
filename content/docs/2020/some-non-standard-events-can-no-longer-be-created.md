---
title: "Some non-standard events can no longer be created"
date: "2020-02-10T22:03:00-05:00"
categories: ["dom"]
tags: []
versions: ["74"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610819"
      title: "Bug 1610819 - Remove support for creating some non-standard event types"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623223"
      title: "Bug 1623223 - CreateEvent regression"
---
Firefox 74 has removed the support for creating several non-standard events with [`document.createEvent()`](https://developer.mozilla.org/docs/Web/API/Document/createEvent). These event types include:

* `KeyEvents` (standard equivalent: `KeyboardEvent`)
* `MouseScrollEvents`
* `ScrollAreaEvent`
* `TimeEvent`

**Update**: One minor website is affected by this change.
