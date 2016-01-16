---
title: "Elements are no longer accessible with the old `id` after being changed"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=790601": "Bug 790601 – Javascript element should not exist with old id"
---
Elements with `id` are accessible as `window.id` DOM objects. Previously, such objects remained on [`window`](https://developer.mozilla.org/en-US/docs/Web/API/window) even after the `id` of the element was programmatically changed. This odd behaviour has been fixed with Firefox 26. The [`document.getElementById`](https://developer.mozilla.org/en-US/docs/Web/API/document.getElementById) method, which is recommended to use in general, is not affected by this change.
