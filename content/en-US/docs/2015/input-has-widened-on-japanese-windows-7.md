---
title: "`<input>` has widened on Japanese Windows 7"
date: "2015-08-16T03:30:08-04:00"
categories: ["html"]
tags: []
versions: "40"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1194055": "Bug 1194055 - Size of <input> elements has changed in Firefox 40"
---
The [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) form control has become wider than previous releases and potentially breaks the page layout on specific environments, the Japanese version of Windows 7 in particular, when no [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) is set on the element. This was due to a change to the default font family on `<input>`. While Mozilla developers are working on a solution, Web developers can work around the issue by explicitly setting a `width` or [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) on the element.

**Update**: This issue has been fixed with Firefox 40.0.3 shipped on <time datetime="2015-08-27">August 27</time>.
