---
title: "`Event.getPreventDefault` has been removed"
date: "2017-11-15T10:25:00-05:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=691151"
      title: "Bug 691151 - Remove Event.prototype.getPreventDefault"
aliases:
    - "/en-CA/docs/2015/event-getpreventdefault-will-be-removed/"
---
The non-standard `Event.prototype.getPreventDefault` method, [deprecated since Firefox 16](https://www.fxsitecompat.com/en-CA/docs/2013/obsolete-event-methods-have-been-removed/), has been removed with Firefox 59 in favour of the standard [`defaultPrevented`](https://developer.mozilla.org/docs/Web/API/Event/defaultPrevented) property.
