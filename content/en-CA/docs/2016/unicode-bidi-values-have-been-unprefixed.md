---
title: "`unicode-bidi` values have been unprefixed"
date: "2016-07-04T14:29:00-04:00"
categories: ["css"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1141895"
      title: "Bug 1141895 - Unprefix values of unicode-bidi"
---
The prefixed values for the [`unicode-bidi`](https://developer.mozilla.org/en-US/docs/Web/CSS/unicode-bidi) CSS property, including `-moz-isolate`, `-moz-isolate-override` and `-moz-plaintext`, can now be used without the vendor prefix. The support for the prefixed values will be removed in the future.
