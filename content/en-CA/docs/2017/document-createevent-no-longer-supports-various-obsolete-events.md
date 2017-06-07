---
title: "`document.createEvent()` no longer supports various obsolete events"
date: "2017-06-07T08:07:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1251198"
      title: "Bug 1251198 - Align document.createEvent() supported events with spec"
---
The support for various obsolete, non-standard events has been removed from the [`document.createEvent`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createEvent) method, including `CommandEvent`, `CommandEvents`, `DataContainerEvent`, `DataContainerEvents`, `DragEvents`, `NotifyPaintEvent`, `PageTransition`, `PopUpEvents`, `SimpleGestureEvent`, `SVGEvent`, `TextEvents` and `TimeEvents`.
