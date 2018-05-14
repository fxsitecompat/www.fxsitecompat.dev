---
title: "`cursor: -moz-zoom-in` and `-moz-zoom-out` have been unprefixed"
date: "2013-05-19T07:35:00-04:00"
categories: ["css"]
tags: []
versions: ["24"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=772153"
      title: "Bug 772153 – unprefix CSS cursor: -moz-zoom-in | -moz-zoom-out"
---
Unprefixed support for the [`-moz-zoom-in`](https://developer.mozilla.org/docs/Web/CSS/-moz-zoom-in) and [`-moz-zoom-out`](https://developer.mozilla.org/docs/Web/CSS/-moz-zoom-out) values for the [`cursor`](https://developer.mozilla.org/docs/Web/CSS/cursor) property has been added. Those were originally Mozilla CSS extensions and are now a part of the CSS3 UI editor's draft. [The prefixed values will be removed](https://bugzilla.mozilla.org/show_bug.cgi?id=879119) after a reasonable period of time.
