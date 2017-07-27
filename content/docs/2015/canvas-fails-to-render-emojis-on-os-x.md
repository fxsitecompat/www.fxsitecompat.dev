---
title: "Canvas fails to render emojis on OS X"
date: "2015-10-03T22:54:00-04:00"
categories: ["canvas-webgl"]
tags: []
versions: ["41"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1209480"
      title: "Bug 1209480 - Canvas no longer able to render emojis (caused by switch to Skia)"
---
The [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) is no longer able to render emoji characters on Firefox 41 and later for the OS X platform, due to the switch to the Skia 2D graphics library. This broke the emoji detection feature of *Modernizr* used by *WordPress* and others. Mozilla developers are working on the solution.

**Update**: This issue has been fixed with Firefox 46.
