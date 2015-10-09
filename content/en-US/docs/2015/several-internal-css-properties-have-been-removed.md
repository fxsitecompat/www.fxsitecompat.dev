---
title: "Several internal CSS properties have been removed"
date: "2015-10-07T01:49:00-04:00"
categories: ["css"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1207002": "Bug 1207002 - Restrict MathML-related internal properties to only be accessible in UA sheets"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1211040": "Bug 1211040 - Restrict -moz-window-{dragging, shadow} to chrome only"
---
Some internal CSS properties for [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) and browser theming, including `-moz-math-display`, `-moz-window-dragging` and [`-moz-window-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-window-shadow), are no longer available from Web content.

**Update**: The `-moz-window-dragging` property has been [restored](https://bugzilla.mozilla.org/show_bug.cgi?id=1212607) due to a compatibility issue with the *Graphene* runtime.
