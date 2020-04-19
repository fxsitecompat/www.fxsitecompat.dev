---
title: "`HTMLInputElement.width` and `height` now return `0` when the `type` is not `image`"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=905240"
      title: "Bug 905240 – HTMLInputElement.{width,height} getter should return 0 for type!=\'image\'"
---
Previously, the `width` and `height` properties of an [`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) returned the dimension of the element. To comply with the spec, those properties now return `0` if the `type` attribute is not `image`.
