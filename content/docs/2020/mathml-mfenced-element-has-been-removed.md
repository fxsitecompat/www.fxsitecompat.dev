---
title: "MathML `<mfenced>` element has been removed"
date: "2020-01-05T17:02:00-05:00"
categories: ["misc"]
tags: []
releases: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1603773"
      title: "Bug 1603773 - Disable the MathML mfenced element by default in all builds"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SJFrpa-UmQk/discussion"
      title: "Intent to unship: MathML mfenced element"
---
The MathML [`<mfenced>`](https://developer.mozilla.org/docs/Web/MathML/Element/mfenced) element deprecated since [Firefox 71](https://www.fxsitecompat.dev/en-CA/docs/2019/various-legacy-mathml-features-have-been-deprecated/) has been removed with Firefox 73. Use the [`<mrow>`](https://developer.mozilla.org/docs/Web/MathML/Element/mrow) and [`<mo>`](https://developer.mozilla.org/docs/Web/MathML/Element/mo) elements instead.
