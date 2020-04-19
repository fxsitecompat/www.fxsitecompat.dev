---
title: "Legacy `-moz-transform` syntax support has been removed"
date: "2018-02-20T01:31:00-05:00"
categories: ["css"]
tags: []
versions: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1438297"
      title: "Bug 1438297 - Unship the legacy syntax for -moz-transform."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/T3PGm97MPNU/discussion"
      title: "Intent to unship: Legacy -moz-transform syntax."
---
Firefox has maintained the legacy syntax support for the `-moz-transform` CSS property that allowed to use lengths or percentages for the `matrix` and `matrix3d` functions, e.g. `matrix(1, 2, 3, 4, 5px, 6%)`. As of Firefox 60, those special cases are no longer handled, and the `-moz`-prefixed property will be a simple alias of the standard [`transform`](https://developer.mozilla.org/docs/Web/CSS/transform) property, just like `-webkit-transform`.

Note that the `-moz-transform` support will be [removed in the future](https://www.fxsitecompat.dev/en-CA/docs/2015/prefixed-css-animations-transforms-transitions-support-will-be-removed/). Make sure you have the standard alternative.
