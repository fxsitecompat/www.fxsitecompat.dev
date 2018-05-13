---
title: "`HTMLMediaElement.src` type has been changed"
date: "2012-12-03T03:50:54-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=792665"
      title: "Bug 792665 – Separate HTMLMediaElement.src from HTMLMediaElement.srcObject"
---
Previously the value of the [`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement)`src` property was a media stream object. In the process of standardization, Mozilla has proposed that the `src` property represents a URL string of the media while the new `srcObject` property has the object. The Firefox implementation has been changed to reflect the proposal. For now, `srcObject` is prefixed `mozSrcObject`.
