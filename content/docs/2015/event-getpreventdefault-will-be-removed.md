---
title: "`Event.getPreventDefault` will be removed"
date: "2015-10-27T22:54:00-07:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=691151"
      title: "Bug 691151 - Remove Event.prototype.getPreventDefault"
---
The non-standard `Event.prototype.getPreventDefault` method, [deprecated since Firefox 16](https://www.fxsitecompat.com/en-CA/docs/2013/obsolete-event-methods-have-been-removed/), will be removed in the future in favour of the standard [`Event.prototype.defaultPrevented`](https://developer.mozilla.org/en-US/docs/Web/API/Event/defaultPrevented) property.
