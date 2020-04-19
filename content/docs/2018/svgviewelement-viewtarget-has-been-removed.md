---
title: "`SVGViewElement.viewTarget` has been removed"
date: "2018-04-25T18:18:00-04:00"
categories: ["dom", "svg"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455763"
      title: "Bug 1455763 - Remove SVGViewElement.viewTarget"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3rbtcFOcVjI/discussion"
      title: "Intent to unship: SVGViewElement.viewTarget"
aliases:
    - "/en-CA/docs/2018/svgviewelement-prototype-viewtarget-has-been-removed/"
---
Firefox 61 has removed the `viewTarget` property from the [`SVGViewElement`](https://developer.mozilla.org/docs/Web/API/SVGViewElement) interface. It was defined in the SVG 1.1 spec but removed with SVG 2 due to lack of use. Also, Firefox didn't have the proper implementation, rather returning an error.

Given that [Google Chrome 56](https://www.chromestatus.com/feature/5665473114931200) shipped in January 2017 has already made the change, the compatibility risk should be low.
