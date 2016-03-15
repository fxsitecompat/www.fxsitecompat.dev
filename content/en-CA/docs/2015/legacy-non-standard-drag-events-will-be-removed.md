---
title: "Legacy non-standard drag events will be removed"
date: "2015-10-25T17:02:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1162050"
      title: "Bug 1162050 - Remove draggesture and dragdrop events"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/thqN2Umpea0/discussion"
      title: "Intent to remove: support for old drag events"
---
The support for the non-standard drag-related events that have been left for backward compatibility will be removed in the near future. The `draggesture` and `dragdrop` events can be replaced with the standard [`dragstart`](https://developer.mozilla.org/en-US/docs/Web/Events/dragstart) and [`drop`](https://developer.mozilla.org/en-US/docs/Web/Events/drop) events respectively. The `dragexit` event will remain because there's no exact standard equivalent, but [`dragleave`](https://developer.mozilla.org/en-US/docs/Web/Events/dragleave) and [`dragend`](https://developer.mozilla.org/en-US/docs/Web/Events/dragend) may work as the alternative in most cases.
