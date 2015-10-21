---
title: "`CSSRule.cssText` now returns unprefixed `writing-mode`-aware properties"
date: "2015-09-22T11:24:00-04:00"
categories: ["css"]
tags: []
versions: ["42"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1118103": "Bug 1118103 - swap the aliasing direction of -moz-margin-start <-> margin-inline-start etc."
---
[Firefox 41](https://developer.mozilla.org/en-US/Firefox/Releases/41#CSS) has enabled the vertical writing support for East Asian scripts by default, adding the [`writing-mode`](https://developer.mozilla.org/en-US/docs/Web/CSS/writing-mode) CSS property and various direction-independent `margin`, `border` and `padding`-related properties. Several existing properties have been [unprefixed](https://www.fxsitecompat.com/en-US/docs/2015/direction-independent-css-properies-have-been-unprefixed/) at the same time.

At the time of the Firefox 41 release, the serialized style rules including property names returned by [`CSSRule.cssText`](https://developer.mozilla.org/en-US/docs/Web/API/CSSRule/cssText), or iteration of the properties in a style rule, were the prefixed, legacy form, like `-moz-margin-start`, rather than the unprefixed, canonical form, like [`margin-inline-start`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-inline-start). The [Page Inspector's CSS pane](https://developer.mozilla.org/en-US/docs/Tools/Page_Inspector/How_to/Examine_and_edit_CSS) was also showing the prefixed properties even though unprefixed ones were already supported. This issue has been fixed with Firefox 42 by swapping the internal alias direction of the prefixed and unprefixed properties.

Those prefixed properties are deprecated and the support will be removed in the future.
