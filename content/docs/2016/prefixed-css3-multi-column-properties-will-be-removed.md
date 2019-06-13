---
title: "Prefixed CSS3 multi-column properties will be removed"
date: "2016-10-10T20:57:00-04:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=698783"
      title: "Bug 698783 - Remove prefixing for CSS3 multicol"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EammrHjrCpw/discussion"
      title: "Intent to ship: css multi-column properties (unprefixed)"
---
The support for the `-moz`-prefixed multi-column properties, [deprecated since Firefox 52](https://www.fxsitecompat.dev/en-CA/docs/2016/css3-multi-column-properties-have-been-unprefixed/), are planned to be removed in the near future. Make sure to use the standard equivalents including [`column-count`](https://developer.mozilla.org/docs/Web/CSS/column-count), [`column-fill`](https://developer.mozilla.org/docs/Web/CSS/column-fill), [`column-gap`](https://developer.mozilla.org/docs/Web/CSS/column-gap), [`column-rule`](https://developer.mozilla.org/docs/Web/CSS/column-rule), [`column-rule-color`](https://developer.mozilla.org/docs/Web/CSS/column-rule-color), [`column-rule-style`](https://developer.mozilla.org/docs/Web/CSS/column-rule-style), [`column-rule-width`](https://developer.mozilla.org/docs/Web/CSS/column-rule-width), [`column-width`](https://developer.mozilla.org/docs/Web/CSS/column-width) and [`columns`](https://developer.mozilla.org/docs/Web/CSS/columns).
