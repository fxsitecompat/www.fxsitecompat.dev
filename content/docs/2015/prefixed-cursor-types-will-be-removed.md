---
title: "Prefixed `cursor` types will be removed"
date: "2015-10-27T18:38:00-07:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=879119"
      title: "Bug 879119 - Drop support for -moz-prefixes from cursor: zoom-in | zoom-out | grab | grabbing"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JhnttZThqts/discussion"
      title: "Intent to unship: -moz-prefixed CSS cursor:zoom-in, zoom-out, grab, grabbing"
---
The prefixed CSS [`cursor`](https://developer.mozilla.org/docs/Web/CSS/cursor) property values, including `-moz-zoom-in`, `-moz-zoom-out`, `-moz-grab` and `-moz-grabbing`, will be removed in the future. [Firefox 24](https://www.fxsitecompat.dev/en-CA/docs/2013/cursor-moz-zoom-in-and-moz-zoom-out-have-been-unprefixed/) has unprefixed `zoom-in` and `zoom-out`, while [Firefox 27](https://www.fxsitecompat.dev/en-CA/docs/2013/moz-grab-and-moz-grabbing-have-been-unprefixed/) has unprefixed `grab` and `grabbing`.
