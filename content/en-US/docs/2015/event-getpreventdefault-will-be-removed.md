---
title: "`Event.getPreventDefault` will be removed"
date: "2015-10-27T22:54:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=691151": "Bug 691151 - Remove Event.prototype.getPreventDefault"
---
The non-standard `Event.prototype.getPreventDefault` method, [deprecated since Firefox 16](https://www.fxsitecompat.com/en-US/docs/2013/obsolete-event-methods-have-been-removed/), will be removed in the future in favor of the standard [`Event.prototype.defaultPrevented`](https://developer.mozilla.org/en-US/docs/Web/API/Event/defaultPrevented) property.
