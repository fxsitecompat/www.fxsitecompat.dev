---
title: "`HTMLMediaElement.srcObject` has been unprefixed"
date: "2015-08-05T00:48:18-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["42", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1175523"
      title: "Bug 1175523 - Unprefix mozSrcObject (to srcObject)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1183495"
      title: "Bug 1183495 - Remove mozSrcObject alias to srcObject soon"
---
The [`srcObject`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/srcObject) property on the [`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) interface has been unprefixed. The prefixed `mozSrcObject` property, which has been kept as an alias, will be removed soon.
