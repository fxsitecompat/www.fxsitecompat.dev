---
title: "`mode` attribute on `<math>` has been removed"
date: "2019-08-15T10:45:00-04:00"
categories: ["misc"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1573438"
      title: "Bug 1573438 - Remove <math>'s mode attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/lZUF2Z9jOh4/discussion"
      title: "Intent to unship: <math>'s mode attribute"
---
The support for the `mode` attribute on the [`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math) element has been dropped with Firefox 70. The attribute had been deprecated since MathML 2 and Firefox 20 in favour of the `display` attribute. It had been implemented only in Firefox and Safari, and will be removed from the MathML 4 spec. A [polyfill](https://github.com/mathml-refresh/mathml/issues/5#issuecomment-521525157) is available for legacy documents.
