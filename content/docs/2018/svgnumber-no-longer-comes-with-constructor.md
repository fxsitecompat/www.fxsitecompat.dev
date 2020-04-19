---
title: "`SVGNumber` no longer comes with constructor"
date: "2018-04-25T12:33:00-04:00"
categories: ["dom", "svg"]
tags: []
releases: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455940"
      title: "Bug 1455940 - Remove constructor from SVGNumber"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/1jEXK-Ctbng/discussion"
      title: "Intent to unship constructors on SVGNumber"
---
The constructor on the [`SVGNumber`](https://developer.mozilla.org/docs/Web/API/SVGNumber) interface has been removed with Firefox 61, because it was not part of the SVG spec and also not implemented in any other browser. Calling `new SVGNumber()` will throw a `TypeError` from now on.
