---
title: "`Accept` header for images has been changed"
date: "2016-03-10T08:02:00-05:00"
categories: ["networking"]
tags: []
versions: ["47"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1249474": "Bug 1249474 - Accept header sent for images prevents w3.org from serving us SVG images in W3C's style sheet"
---
Firefox was previously sending `image/png,image/*;q=0.8,*/*;q=0.5` as the [`Accept` HTTP header's value for images](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#Values_for_an_image). This value is not so meaningful at this time since PNG images have become widely used, therefore Firefox 47 and later sends `*/*` instead, just like Safari. Once Firefox [supports the WebP image format](https://bugzilla.mozilla.org/show_bug.cgi?id=856375), it will probably be changed to `image/webp,*/*`.
