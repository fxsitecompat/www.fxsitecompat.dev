---
title: "Fullscreen request is now only allowed on HTML elements, `<svg>` and `<math>`"
date: "2016-10-16T03:06:00-04:00"
categories: ["dom"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305928"
      title: "Bug 1305928 - Fullscreen request should only be allowed for HTML element, <svg>, and <math>"
---
On Firefox 52 and later, the [`Element.requestFullscreen`](https://developer.mozilla.org/docs/Web/API/Element/requestFullscreen) method can no longer be used for elements other than HTML elements, [`<svg>`](https://developer.mozilla.org/docs/Web/SVG/Element/svg) and [`<math>`](https://developer.mozilla.org/docs/Web/MathML/Element/math), according to the latest Fullscreen API spec. Note that the method is [still prefixed](https://www.fxsitecompat.dev/en-CA/docs/2016/fullscreen-api-has-been-unprefixed-in-non-release-builds/) on the Firefox Beta and Release channels.
