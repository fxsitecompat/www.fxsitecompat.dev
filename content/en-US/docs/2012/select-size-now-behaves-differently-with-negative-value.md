---
title: "`select.size` now behaves differently with negative value"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: "16"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=760848": "Bug 760848 – select.size reflection is wrong"
---
The [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) element no longer throws when a negative value is provided to the `size` property, that is now rather considered as `0`.
