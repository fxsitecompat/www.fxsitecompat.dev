---
title: "`MouseEvent.mozPressure` has been deprecated"
date: "2019-05-28T03:35:00-04:00"
categories: ["dom"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165211"
      title: "Bug 1165211 - Deprecate MouseEvent.mozPressure"
aliases:
    - "/en-CA/docs/2015/mouseevent-mozpressure-will-be-removed/"
---
The `mozPressure` property on the `MouseEvent` interface is now deprecated and will be removed in the near future. Firefox 68 will show a deprecation warning in the console when the property is found on a page. Use the standard [`PointerEvent.pressure`](https://developer.mozilla.org/docs/Web/API/PointerEvent/pressure) property instead, which is part of the Pointer Events API available since Firefox 59.
