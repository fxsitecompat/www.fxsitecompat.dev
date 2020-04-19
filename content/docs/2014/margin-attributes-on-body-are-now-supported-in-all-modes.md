---
title: "Margin attributes on `<body>` are now supported in all modes"
date: "2014-10-17T22:50:44-04:00"
categories: ["html"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=95530"
      title: "Bug 95530 – topmargin and leftmargin attributes on the BODY element should be honored in all modes (not just Quirks mode)"
---
The [`body`](https://developer.mozilla.org/docs/Web/HTML/Element/body) element's non-standard `topmargin`, `bottommargin`, `rightmargin` and `leftmargin` attributes, previously supported only in the [Quirks mode](https://developer.mozilla.org/docs/Mozilla_Quirks_Mode_Behavior) for compatibility with Internet Explorer, are now honored in the Standards compliance mode too, because they are now a part of the HTML5 spec.
