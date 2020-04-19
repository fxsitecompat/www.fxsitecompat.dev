---
title: "`<altGlyph>` is no longer supported"
date: "2016-05-10T19:51:00-04:00"
categories: ["svg"]
tags: []
versions: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260032"
      title: "Bug 1260032 - drop support for altGlyph"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/LcN2jd9gGiM/discussion"
      title: "Intent to unship support for altGlyph"
---
The support for the [`<altGlyph>`](https://developer.mozilla.org/docs/Web/SVG/Element/altGlyph) element has been dropped from Firefox due to the removal from the SVG2 spec. It had been an alias of [`<tspan>`](https://developer.mozilla.org/docs/Web/SVG/Element/tspan) that can be used instead.
