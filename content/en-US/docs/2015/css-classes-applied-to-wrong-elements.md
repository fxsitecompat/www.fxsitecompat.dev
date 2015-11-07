---
title: "CSS classes applied to wrong elements"
date: "2015-11-07T00:03:00-08:00"
categories: ["css"]
tags: []
versions: ["42", "43", "44", "45"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1222226": "Bug 1222226 - CSS class applied to wrong elements"
---
Firefox 42 has introduced a regression where CSS classes programmatically added with [`Element.className`](https://developer.mozilla.org/en-US/docs/Web/API/Element/className), for example, at a certain timing are applied to wrong elements, leading to unexpected page styling. Mozilla developers are working on the solution.
