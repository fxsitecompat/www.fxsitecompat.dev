---
title: "`font-feature-settings` has been unprefixed while the newly enabled `font-variant-*` properties are preferred"
date: "2014-09-01T22:12:15-04:00"
categories: ["css"]
tags: []
releases: ["34", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=835191"
      title: "Bug 835191 – Unprefix -moz-font-feature-settings"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=975744"
      title: "Bug 975744 – enable font-variant-* / font-feature in release by default"
---
The following properties defined in the CSS3 Fonts Module spec are now enabled by default: [`font-kerning`](https://developer.mozilla.org/docs/Web/CSS/font-kerning), [`font-synthesis`](https://developer.mozilla.org/docs/Web/CSS/font-synthesis), [`font-variant`](https://developer.mozilla.org/docs/Web/CSS/font-variant), [`font-variant-alternates`](https://developer.mozilla.org/docs/Web/CSS/font-variant-alternates), [`font-variant-caps`](https://developer.mozilla.org/docs/Web/CSS/font-variant-caps), [`font-variant-east-asian`](https://developer.mozilla.org/docs/Web/CSS/font-variant-east-asian), [`font-variant-ligatures`](https://developer.mozilla.org/docs/Web/CSS/font-variant-ligatures), [`font-variant-numeric`](https://developer.mozilla.org/docs/Web/CSS/font-variant-numeric) and [`font-variant-position`](https://developer.mozilla.org/docs/Web/CSS/font-variant-position).

At the same time, the [`font-feature-settings`](https://developer.mozilla.org/docs/Web/CSS/font-feature-settings) and [`font-language-override`](https://developer.mozilla.org/docs/Web/CSS/font-language-override) properties have been unprefixed, the prefixed properties therefore will be removed in the future. From now on, Web authors are recommended to use the new, comprehensible `font-variant-*` properties instead of the low-level `font-feature-settings` property.
