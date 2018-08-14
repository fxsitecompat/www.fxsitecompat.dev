---
title: "Several non-standard `overflow` property values have been dropped"
date: "2018-08-14T14:08:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1481125"
      title: "Bug 1481125 - Tracking -moz-scrollbars-none when creating webcompat issues."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/rujif05uOTo/discussion"
      title: "Intent to unship: overflow: -moz-scrollbars-* values"
---
The following non-standard, prefixed values for the [`overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow) CSS property have been disabled by default in favour of the standard alternatives:

* `-moz-scrollbars-none`
    * Use `overflow: hidden` instead
* `-moz-scrollbars-horizontal`
    * Use `overflow: scroll hidden` or `overflow-x: scroll; overflow-y: hidden` instead
* `-moz-scrollbars-vertical`
    * Use `overflow: hidden scroll` or `overflow-x: hidden; overflow-y: scroll` instead

`-moz-hidden-unscrollable` is now the only prefixed value for the property, though it's not for general purposes.
