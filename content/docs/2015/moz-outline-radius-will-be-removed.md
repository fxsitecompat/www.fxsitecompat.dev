---
title: "`-moz-outline-radius` will be removed"
date: "2015-10-27T18:02:00-07:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=315209"
      title: "Bug 315209 - outline should follow shape of border-radius (remove -moz-outline-radius)"
---
The non-standard [`-moz-outline-radius`](https://developer.mozilla.org/docs/Web/CSS/-moz-outline-radius), [`-moz-outline-radius-topright`](https://developer.mozilla.org/docs/Web/CSS/-moz-outline-radius-topright), [`-moz-outline-radius-topleft`](https://developer.mozilla.org/docs/Web/CSS/-moz-outline-radius-topleft), [`-moz-outline-radius-bottomright`](https://developer.mozilla.org/docs/Web/CSS/-moz-outline-radius-bottomright) and [`-moz-outline-radius-bottomleft`](https://developer.mozilla.org/docs/Web/CSS/-moz-outline-radius-bottomleft) CSS properties will be removed in the future because those are not a part of the spec. An [`outline`](https://developer.mozilla.org/docs/Web/CSS/outline) should follow the shape of [`border-radius`](https://developer.mozilla.org/docs/Web/CSS/border-radius).
