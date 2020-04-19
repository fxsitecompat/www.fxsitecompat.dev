---
title: "SVG `preserveAspectRatio` no longer supports `defer` option"
date: "2016-08-03T10:40:00-04:00"
categories: ["svg"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1280425"
      title: "Bug 1280425 - Drop support for SVG <image preserveAspectRatio=\"defer ...\">"
---
The support for the `defer` keyword for the [`preserveAspectRatio`](https://developer.mozilla.org/docs/Web/SVG/Attribute/preserveAspectRatio) attribute on the [`<image>`](https://developer.mozilla.org/docs/Web/SVG/Element/image) element has been dropped because of the removal from the SVG2 spec.
