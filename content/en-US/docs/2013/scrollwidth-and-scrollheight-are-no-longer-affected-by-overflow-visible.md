---
title: "`scrollWidth` and `scrollHeight` are no longer affected by `overflow:visible`"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=833542": "Bug 833542 – scrollWidth, scrollHeight different when overflow is hidden versus visible"
---
The [`scrollWidth`](https://developer.mozilla.org/en-US/docs/Web/API/element.scrollWidth) and [`scrollHeight`](https://developer.mozilla.org/en-US/docs/Web/API/element.scrollHeight) properties might have wrong values when CSS `overflow:visible` was set on the element. This behavior has been fixed to match the values as if `overflow:hidden` is set.
