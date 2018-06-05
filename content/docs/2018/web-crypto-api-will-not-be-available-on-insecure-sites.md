---
title: "Web Crypto API will not be available on insecure sites"
date: "2018-06-05T10:54:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333140"
      title: "Bug 1333140 - Require [SecureContext] for Web Crypto"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/55t-Uyx1TxI/discussion"
      title: "Intent to Remove: Insecure use of WebCrypto"
---
The [Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) will only work on secure sites served over HTTPS in the near future, as required by the current spec. Given that [Google Chrome 60](https://developers.google.com/web/updates/2017/06/chrome-60-deprecations) shipped in July 2017 has already made the change, the compatibility risk should be low.
