---
title: "`unicode-bidi` values have been unprefixed"
date: "2016-07-04T14:29:00-04:00"
categories: ["css"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1141895"
      title: "Bug 1141895 - Unprefix values of unicode-bidi"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/O9DrBrXvH14/discussion"
      title: "Intent to ship: unprefixed unicode-bidi values"
---
The prefixed values for the [`unicode-bidi`](https://developer.mozilla.org/docs/Web/CSS/unicode-bidi) CSS property, including `-moz-isolate`, `-moz-isolate-override` and `-moz-plaintext`, can now be used without the vendor prefix. The support for the prefixed values will be removed in the future.

**Update**: The prefix support has been removed with [Firefox 54](https://www.fxsitecompat.com/en-CA/docs/2017/prefixed-unicode-bidi-values-are-no-longer-supported/).
