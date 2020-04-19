---
title: "`scrollWidth` and `scrollHeight` are no longer affected by `overflow:visible`"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=833542"
      title: "Bug 833542 – scrollWidth, scrollHeight different when overflow is hidden versus visible"
---
The [`scrollWidth`](https://developer.mozilla.org/docs/Web/API/element.scrollWidth) and [`scrollHeight`](https://developer.mozilla.org/docs/Web/API/element.scrollHeight) properties might have wrong values when CSS `overflow:visible` was set on the element. This behaviour has been fixed to match the values as if `overflow:hidden` is set.
