---
title: "Legacy non-standard drag events have been removed"
date: "2016-07-13T14:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["50"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1162050"
      title: "Bug 1162050 - Remove draggesture and dragdrop events"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/thqN2Umpea0/discussion"
      title: "Intent to remove: support for old drag events"
aliases:
    - "/en-CA/docs/2015/legacy-non-standard-drag-events-will-be-removed/"
---
The support for the non-standard drag-related events that had been left for backward compatibility has been removed with Firefox 50. The `draggesture` and `dragdrop` events should be replaced with the standard [`dragstart`](https://developer.mozilla.org/docs/Web/Events/dragstart) and [`drop`](https://developer.mozilla.org/docs/Web/Events/drop) events respectively. Meanwhile, the [`dragexit`](https://developer.mozilla.org/docs/Web/Events/dragexit) event has been standardized so you don't have to care about it anymore.

**Update**: This change seems to be affecting several sites including *NFL.com* and *TweetDeck*.
