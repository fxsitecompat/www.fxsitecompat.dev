---
title: "Support for EME on insecure contexts has been deprecated"
date: "2017-05-04T17:21:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1322517"
      title: "Bug 1322517 - [EME] Remove support for EME on insecure contexts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1361000"
      title: "Bug 1361000 - Add deprecation warning for removing support for EME on insecure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/sa_2q8oEKgE/discussion"
      title: "Intent to remove: Insecure use of Encrypted Media Extensions"
---
The [Encrypted Media Extensions (EME) API](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API), used by publishers like *Netflix* to serve DRM-protected content, can only be used on [secure contexts](https://developer.mozilla.org/docs/Web/Security/Secure_Contexts) according to the latest spec. In Firefox, the support for EME on insecure contexts is now deprecated with a console warning and will be removed in the near future.
