---
title: "Prefixed `unicode-bidi` values are no longer supported"
date: "2017-02-09T03:55:00-05:00"
categories: ["css"]
tags: []
versions: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333675"
      title: "Bug 1333675 - Consider removing prefixed value of unicode-bidi"
---
The support for the vendor-prefixed [`unicode-bidi`](https://developer.mozilla.org/docs/Web/CSS/unicode-bidi) CSS property values, deprecated since [Firefox 50](https://www.fxsitecompat.dev/en-CA/docs/2016/unicode-bidi-values-have-been-unprefixed/), has been removed with Firefox 54. Use the unprefixed values instead of `-moz-isolate`, `-moz-isolate-override` and `-moz-plaintext`.
