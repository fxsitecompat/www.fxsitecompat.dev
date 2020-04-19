---
title: "Several non-standard `overflow` property values have been dropped"
date: "2018-08-14T14:08:00-04:00"
categories: ["css"]
tags: []
versions: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1481125"
      title: "Bug 1481125 - Tracking -moz-scrollbars-none when creating webcompat issues."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/rujif05uOTo/discussion"
      title: "Intent to unship: overflow: -moz-scrollbars-* values"
---
The following non-standard, prefixed values for the [`overflow`](https://developer.mozilla.org/docs/Web/CSS/overflow) CSS property have been disabled by default in favour of the standard alternatives:

* `-moz-scrollbars-none`
    * Use `overflow: hidden` instead
* `-moz-scrollbars-horizontal`
    * Use `overflow-x: scroll; overflow-y: hidden` instead
    * <del>`overflow: hidden scroll` can also be used on [Firefox 63 and later](https://www.fxsitecompat.dev/en-CA/docs/2018/overflow-shorthand-syntax-has-been-updated-to-swap-2-values/)</del>
* `-moz-scrollbars-vertical`
    * Use `overflow-x: hidden; overflow-y: scroll` instead
    * <del>`overflow: scroll hidden` can also be used on [Firefox 63 and later](https://www.fxsitecompat.dev/en-CA/docs/2018/overflow-shorthand-syntax-has-been-updated-to-swap-2-values/)</del>

`-moz-hidden-unscrollable` is now the only prefixed value for the property, though it's not for general purposes.
