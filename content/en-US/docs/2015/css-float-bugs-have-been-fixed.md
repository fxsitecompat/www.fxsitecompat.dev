---
title: "CSS `float` bugs have been fixed"
date: "2015-09-23T07:14:00-04:00"
categories: ["css"]
tags: []
versions: ["42"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=451791": "Bug 451791 - CSS margin-top collapses across cleared element inside previous sibling and out top of previous sibling (works in Safari, but Firefox has a bug)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=478834": "Bug 478834 - table (or other BFC) following float doesn't clear it even if it can't fit next to it, when lined up at their tops"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=538194": "Bug 538194 - non-floated block formatting context only checks top edge for overlap with floats rather than entire height"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1196255": "Bug 1196255 - tabzilla invisible on mobile view of /privacy/tips/"
---
A couple of longstanding issues regarding CSS [`float`](https://developer.mozilla.org/en-US/docs/Web/CSS/float) handling have been fixed with Firefox 42. 

In the first bug, the `margin-top` and `margin-bottom` properties were wrongly applied when used in conjunction with the `float` property under certain circumstances. In the second bug, a `<table>` after a floated element was not cleared properly, resulting in overlapped content. In the third bug, two floated elements with different widths led to a misplacement of the subsequent element, resulting in overlapped content as well.

While those changes should align with the specification and other browsers' behavior, some pages may be broken if those are relying on the previous behavior of Firefox. Actually, Mozilla's own site is known to be affected.
