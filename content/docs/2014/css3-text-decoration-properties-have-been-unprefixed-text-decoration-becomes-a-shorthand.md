---
title: "CSS3 Text Decoration properties have been unprefixed, `text-decoration` becomes a shorthand"
date: "2014-12-19T11:15:21-05:00"
categories: ["css"]
tags: []
versions: ["36"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=825004"
      title: "Bug 825004 – [css-text-decor-3] Unprefix CSS3 Text Decoration"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1039488"
      title: "Bug 1039488 – support the full css3-text-decor syntax for the \'text-decoration\' shorthand rather than only the CSS2.1 syntax"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1097922"
      title: "Bug 1097922 – Remove temporary aliases for -moz-text-decoration-*."
---
The [`text-decoration`](https://developer.mozilla.org/docs/Web/CSS/text-decoration) property is now compatible with [CSS3 Text Decoration Module Level 3](https://drafts.csswg.org/css-text-decor-3/), and the following properties defined in the spec are now unprefixed: [`text-decoration-line`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-line), [`text-decoration-color`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-color) and [`text-decoration-style`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-style). `text-decoration` has become a [shorthand property](https://developer.mozilla.org/docs/Web/CSS/Shorthand_properties) but will behave as before like CSS 2.1 as if both `text-decoration-color` and `text-decoration-style` are the [initial values](https://developer.mozilla.org/docs/Web/CSS/initial_value). The prefixed `-moz-text-decoration-*` properties are still supported, but will be removed in a few releases.

**Update**: Those prefixed properties have been [removed with Firefox 40](https://www.fxsitecompat.com/en-CA/docs/2015/moz-text-decoration-properties-have-been-removed/).
