---
title: "Various legacy MathML features have been deprecated"
date: "2019-10-07T08:03:00-04:00"
categories: ["misc"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548522"
      title: "Bug 1548522 - Remove support for the menclose's \"radical\" notation"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548530"
      title: "Bug 1548530 - Remove support for numalign/denomalign/align attributes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575870"
      title: "Bug 1575870 - Remove support for XLink on MathML elements"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vwAkuZIEhnY/discussion"
      title: "Intent to unship: MathML menclose notation \"radical\""
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JnJVGTmIwPE/discussion"
      title: "Intent to unship: MathML alignment attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/70NFnet82cU/discussion"
      title: "Intend to deprecate: XLink attributes on MathML elements"
---
As with [Firefox 70](https://www.fxsitecompat.dev/en-CA/docs/2019/various-legacy-mathml-features-have-been-deprecated-or-removed/), the MathML implementation has been updated with Firefox 71 for the current MathML Core (future MathML 4) spec. The following features are now deprecated, disabled in Firefox Nightly and will be removed in the future:

* The `align` attribute on the [`<munderover>`](https://developer.mozilla.org/docs/Web/MathML/Element/munderover), [`<munder>`](https://developer.mozilla.org/docs/Web/MathML/Element/munder) and [`<mover>`](https://developer.mozilla.org/docs/Web/MathML/Element/mover) elements
* The `denomalign` and `numalign` attributes on the [`<mfrac>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfrac) element
* The `radical` value for the [`<menclose>`](https://developer.mozilla.org/docs/Web/MathML/Element/menclose) element's `notation` attribute. Use the [`<msqrt>`](https://developer.mozilla.org/docs/Web/MathML/Element/msqrt) element instead
* [XLink](https://developer.mozilla.org/docs/Glossary/XLink) attributes on MathML elements: `xlink:actuate`, `xlink:href`, `xlink:show` and `xlink:type`. The `href` attribute can be used instead of `xlink:href`
