---
title: "`::placeholder` pseudo-element and `:placeholder-shown` pseudo-class have been unprefixed"
date: "2016-09-07T18:29:00-04:00"
categories: ["css"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1069012"
      title: "Bug 1069012 - unprefix :placeholder-shown pseudo-class and ::placeholder pseudo-element"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1069015"
      title: "Bug 1069015 - restore code for :placeholder-shown pseudo-class"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1300896"
      title: "Bug 1300896 - Remove prefixed ::-moz-placeholder pseudo-element and pseudo-class."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ZdfheO1AXP0/discussion"
      title: "Intent to ship: CSS placeholder pseudo-element"
---
The [`::placeholder`](https://developer.mozilla.org/docs/Web/CSS/::placeholder) CSS pseudo-element has been unprefixed so that [`::-moz-placeholder`](https://developer.mozilla.org/docs/Web/CSS/::-moz-placeholder) is now deprecated. Also, `:placeholder-shown` has been added as the standard equivalent of the [`:-moz-placeholder`](https://developer.mozilla.org/docs/Web/CSS/:-moz-placeholder) pseudo-class [deprecated since Firefox 19](https://www.fxsitecompat.dev/en-CA/docs/2012/moz-placeholder-pseudo-class-has-been-replaced-with-the-pseudo-element/). The support for each prefixed version will be removed in the future.
