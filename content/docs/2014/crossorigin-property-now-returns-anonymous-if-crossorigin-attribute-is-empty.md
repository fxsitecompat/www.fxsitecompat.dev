---
title: "`crossOrigin` property now returns `anonymous` if `crossorigin` attribute is empty"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=880997"
      title: "Bug 880997 – Reflect crossOrigin as a limited enumerated attribute"
---
The [`crossOrigin`](https://developer.mozilla.org/docs/Web/HTML/CORS_settings_attributes) property of HTML media elements now returns `"anonymous"` when the `crossorigin` attribute of the element is empty. This change has been made in order to distinguish such a case from missing attribute that also returns an empty string.
