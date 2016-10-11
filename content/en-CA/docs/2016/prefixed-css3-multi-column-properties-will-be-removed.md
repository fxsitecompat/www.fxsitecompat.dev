---
title: "Prefixed CSS3 multi-column properties will be removed"
date: "2016-10-10T20:57:00-04:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308636"
      title: "Bug 1308636 - Remove support for prefixed CSS multi column properties by removing aliases for these prefixed properties in nsCSSPropAliasList.h and property_database.js"
---
The support for the `-moz`-prefixed multi-column properties, [deprecated since Firefox 52](https://www.fxsitecompat.com/en-CA/docs/2016/css3-multi-column-properties-have-been-unprefixed/), are planned to be removed in the near future. Make sure to use the standard equivalents including [`column-count`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-count), [`column-fill`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-fill), [`column-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-gap), [`column-rule`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule), [`column-rule-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule-color), [`column-rule-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule-style), [`column-rule-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-rule-width), [`column-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-width) and [`columns`](https://developer.mozilla.org/en-US/docs/Web/CSS/columns).
