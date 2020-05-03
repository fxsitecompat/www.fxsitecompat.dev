---
title: "Various legacy MathML features have been deprecated"
date: "2019-10-07T08:03:00-04:00"
categories: ["misc"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548522"
      title: "Bug 1548522 - Remove support for the menclose's \"radical\" notation"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548530"
      title: "Bug 1548530 - Remove support for numalign/denomalign/align attributes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575870"
      title: "Bug 1575870 - Remove support for XLink on MathML elements"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587570"
      title: "Bug 1587570 - Remove support for the subscriptshift and superscriptshift attributes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587572"
      title: "Bug 1587572 - Remove support for the mfrac@bevelled attribute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587577"
      title: "Bug 1587577 - Remove support for the mfenced element"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vwAkuZIEhnY/discussion"
      title: "Intent to unship: MathML menclose notation \"radical\""
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JnJVGTmIwPE/discussion"
      title: "Intent to unship: MathML alignment attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/70NFnet82cU/discussion"
      title: "Intend to deprecate: XLink attributes on MathML elements"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/CAqw0Nxw6Pg/discussion"
      title: "Intent to deprecate: MathML subscriptshift and superscriptshift attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/9pEvlYn-Xyw/discussion"
      title: "Intent to deprecate: MathML bevelled attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DHO72glZxA0/discussion"
      title: "Intent to deprecated: mfenced element"
supported_tools:
  firefox_extension: true
---
As with [Firefox 70](https://www.fxsitecompat.dev/en-CA/docs/2019/various-legacy-mathml-features-have-been-deprecated-or-removed/), the MathML implementation has been updated with Firefox 71 for the current MathML Core (future MathML 4) spec. The following features are now deprecated, disabled in Firefox Nightly and will be removed in the future:

* The `align` attribute on the [`<munderover>`](https://developer.mozilla.org/docs/Web/MathML/Element/munderover), [`<munder>`](https://developer.mozilla.org/docs/Web/MathML/Element/munder) and [`<mover>`](https://developer.mozilla.org/docs/Web/MathML/Element/mover) elements
* The `bevelled`, `denomalign` and `numalign` attributes on the [`<mfrac>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfrac) element
* The `radical` value for the [`<menclose>`](https://developer.mozilla.org/docs/Web/MathML/Element/menclose) element's `notation` attribute. Use the [`<msqrt>`](https://developer.mozilla.org/docs/Web/MathML/Element/msqrt) element instead
* The `subscriptshift` and `superscriptshift` attributes on the [`<msubsup>`](https://developer.mozilla.org/docs/Web/MathML/Element/msubsup), [`<msub>`](https://developer.mozilla.org/docs/Web/MathML/Element/msub) and [`<msup>`](https://developer.mozilla.org/docs/Web/MathML/Element/msup) elements
* The [`<mfenced>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfenced) element. Use the [`<mrow>`](https://developer.mozilla.org/docs/Web/MathML/Element/mrow) and [`<mo>`](https://developer.mozilla.org/docs/Web/MathML/Element/mo) elements instead
* [XLink](https://developer.mozilla.org/docs/Glossary/XLink) attributes on MathML elements: `xlink:actuate`, `xlink:href`, `xlink:show` and `xlink:type`. The `href` attribute can be used instead of `xlink:href`
