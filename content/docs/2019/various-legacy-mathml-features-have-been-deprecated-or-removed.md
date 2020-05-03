---
title: "Various legacy MathML features have been deprecated or removed"
date: "2019-09-05T01:34:00-04:00"
categories: ["misc"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548524"
      title: "Bug 1548524 - Remove attributes deprecated from MathML3"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548527"
      title: "Bug 1548527 - Remove \"small\" \"normal\" \"big\" values of mathsize"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1548529"
      title: "Bug 1548529 - Remove values \"thin\", \"thick\", \"medium\" values of mfrac@linethickness"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1573438"
      title: "Bug 1573438 - Remove <math>'s mode attribute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574749"
      title: "Bug 1574749 - Remove support for nonzero unitless lengths"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574750"
      title: "Bug 1574750 - Remove support for MathML length values thinmathspace, mediummathspace, thickmathspace, etc"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575542"
      title: "Bug 1575542 - Add counter and warnings for deprecated MathML lengths"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1575596"
      title: "Bug 1575596 - MathML Lengths: Do not accept numbers ending with a dot"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/kl5c87mBlO0/discussion"
      title: "Intent to unship: Deprecated MathML style attributes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/kyB34PjYXek/discussion"
      title: "Intent to deprecate: named values the mathsize attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/G91-vBeC3Rw/discussion"
      title: "Intent to deprecate: named values for <mfrac>'s linethickness attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/lZUF2Z9jOh4/discussion"
      title: "Intent to unship: <math>'s mode attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/-yV6wb3klSA/discussion"
      title: "Intent to unship: nonzero unitless MathML lengths"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/yEMdIOo4i-0/discussion"
      title: "Intent to deprecate: mathspace names for MathML lengths"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wIjm9JjVHNg/discussion"
      title: "Intent to unship: Legacy MathML syntax for numbers"
aliases:
    - "/en-CA/docs/2019/mode-attribute-on-math-has-been-removed/"
supported_tools:
  firefox_extension: true
---
Firefox 70 has updated the MathML implementation in an effort to comply with the current MathML Core (future MathML 4) spec.

The following features are implemented in WebKit as well, but now are deprecated, disabled in Firefox Nightly and will be removed in the future:

* Named values for the `linethickness` attribute on the [`<mfrac>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfrac) element, including `thin`, `medium` and `thick`
* Named values for the `mathsize` attribute on the [`<mtext>`](https://developer.mozilla.org/docs/Web/MathML/Element/mtext) and other elements, including `small`, `normal` and `big`
* Named length values including `veryverythinmathspace`, `verythinmathspace`, `thinmathspace`, `mediummathspace`, `thickmathspace`, `verythickmathspace`, `veryverythickmathspace`, `negativeveryverythinmathspace`, `negativeverythinmathspace`, `negativethinmathspace`, `negativemediummathspace`, `negativethickmathspace`, `negativeverythickmathspace` and `negativeverythickmathspace`. See [this conversion](https://github.com/mathml-refresh/mathml/issues/75#issuecomment-523016332) if needed
* Style attributes including `background`, `color`, `fontfamily`, `fontsize`, `fontstyle` and `fontweight`, which have been deprecated since Firefox 20. Use `mathbackground`, `mathcolor`, `mathsize` and `mathvariant` instead

The following features have been removed:

* The `mode` attribute on the [`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math) element, which was implemented only in Firefox and deprecated since Firefox 20 in favour of the `display` attribute. A [polyfill](https://github.com/mathml-refresh/mathml/issues/5#issuecomment-521525157) is available for legacy documents
* Non-zero unitless length values, such as `5` for 500%, which have been deprecated since Firefox 20
* Length values ending with a dot, such as `2.` or `34.px`
