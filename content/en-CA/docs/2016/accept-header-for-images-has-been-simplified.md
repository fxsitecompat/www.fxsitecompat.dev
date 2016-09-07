---
title: "`Accept` header for images has been simplified"
date: "2016-03-10T08:02:00-05:00"
categories: ["networking"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249474"
      title: "Bug 1249474 - Accept header sent for images prevents w3.org from serving us SVG images in W3C's style sheet"
aliases:
    - "/docs/2016/accept-header-for-images-has-been-changed/"
---
Firefox was previously sending `image/png,image/*;q=0.8,*/*;q=0.5` as the [`Accept` HTTP header's value for images](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation/List_of_default_Accept_values#Values_for_an_image). This value is not so meaningful at this time since PNG images have become widely used, and *W3C*'s site also has a compatibility issue where Firefox gets served PNG instead of SVG, therefore Firefox 47 and later sends `*/*` instead, just like Safari. Once Firefox [supports the WebP image format](https://bugzilla.mozilla.org/show_bug.cgi?id=856375), it will probably be changed to `image/webp,*/*`.
