---
title: "`CSSRule.selectorText` now returns two colons for pseudo-elements"
date: "2014-12-19T11:15:21-05:00"
categories: ["css"]
tags: []
releases: ["36", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949651"
      title: "Bug 949651 – Pseudo-elements should always be separated by two colons in selectorText"
---
The [`::before`](https://developer.mozilla.org/docs/Web/CSS/::before), [`::after`](https://developer.mozilla.org/docs/Web/CSS/::after), [`::first-letter`](https://developer.mozilla.org/docs/Web/CSS/::first-letter), and [`::first-line`](https://developer.mozilla.org/docs/Web/CSS/::first-line) pseudo-elements are now returned with double colons (`::`) as defined in the CSS3 spec, when accessed with the [`CSSStyleRule.selectorText`](https://developer.mozilla.org/docs/Web/API/CSSStyleRule/selectorText) CSSOM property. Previously this property was returning those pseudo-elements in the CSS2 single colon (`:`) syntax.
