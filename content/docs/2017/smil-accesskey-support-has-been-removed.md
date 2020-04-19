---
title: "SMIL `accessKey` support has been removed"
date: "2017-12-12T15:31:00-05:00"
categories: ["svg"]
tags: []
versions: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1423098"
      title: "Bug 1423098 - Remove support for SMIL's accessKey feature"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/skw-Yj_Pdjk/discussion"
      title: "Intent to unship: SMIL accessKey support"
---
Synchronized Multimedia Integration Language (SMIL) includes a feature to trigger SVG animations when a specific key is pressed, like the HTML [`accesskey`](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/accesskey) attribute. This can be defined by web developers using the `begin` attribute with an `accessKey` value. However, no other browsers than Firefox support this at this time, and it has also been the source of several security issues. Given that, the `accessKey` support has been dropped with Firefox 59.
