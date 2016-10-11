---
title: "CSS3 multi-column properties have been unprefixed"
date: "2016-10-10T20:34:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1300895"
      title: "Bug 1300895 - Unprefix css3 multi-column properties (and add back -moz prefixed versions as aliases, for now)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=616436"
      title: "Bug 616436 - column-span not implemented (css3 multicolumn)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EammrHjrCpw/discussion"
      title: "Intent to ship: css multi-column properties (unprefixed)"
---
The [`column-count`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-count), [`column-fill`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-fill), [`column-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-gap), [`column-rule`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule), [`column-rule-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule-color), [`column-rule-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule-style), [`column-rule-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule-width), [`column-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-width) and [`columns`](https://developer.mozilla.org/en-US/docs/Web/CSS/columns) properties have been unprefixed with Firefox 52. The `-moz`-prefixed versions will remain as the aliases but be [removed in the near future](https://www.fxsitecompat.com/en-CA/docs/2016/prefixed-css3-multi-column-properties-will-be-removed/).

Note that the [`column-span`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-span) property is not yet supported in Firefox.
