---
title: "`dominant-baseline` is now inherited from its parent element"
date: "2019-07-21T20:10:00-04:00"
categories: ["css", "svg"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1353164"
      title: "Bug 1353164 - dominant-baseline will become inherited in SVG 2 (and CSS Inline 3)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JjSHhxIn1Wk/discussion"
      title: "Intent to change: dominant-baseline to inherit"
---
The [`dominant-baseline`](https://developer.mozilla.org/docs/Web/SVG/Attribute/dominant-baseline) attribute was not inherited in SVG 1.1 but is inherited in SVG 2, where the attribute is defined in CSS 3 as the `dominant-baseline` property. Firefox 70 has made the inheritance change to comply with the current spec.
