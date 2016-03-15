---
title: "`displaystyle` is no longer inherited from the root `<math>` element"
date: "2014-02-07T11:57:09-05:00"
categories: ["mathml"]
tags: []
versions: ["29"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=838506"
      title: "Bug 838506 – Refactor implementation of displaystyle using a -moz-display-style property"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1011237"
      title: "Bug 1011237 – Explicit displaystyle=\"true\" on root <math> element is not inherited"
---
The implementation of the `displaystyle` attribute has been refactored to adhere to the spec. `displaystyle` on the [`<mtable>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/mtable) element is no longer inherited from the root [`<math>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/math) element. If the attribute is not present, it is considered as `false`, the default value of `displaystyle`. See the [default stylesheet](http://mxr.mozilla.org/mozilla-release/source/layout/mathml/mathml.css) for how it works.
