---
title: "Web Crypto API is no longer available on insecure sites"
date: "2020-02-12T00:16:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333140"
      title: "Bug 1333140 - Require [SecureContext] for Web Crypto"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/55t-Uyx1TxI/discussion"
      title: "Intent to Remove: Insecure use of WebCrypto"
aliases:
    - "/en-CA/docs/2018/web-crypto-api-will-not-be-available-on-insecure-sites/"
---
Starting with Firefox 75, the [Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) will only work on secure sites served over HTTPS, as required by the current spec. `window.crypto.subtle` will be `undefined` on insecure sites. Given that [Google Chrome 60](https://developers.google.com/web/updates/2017/06/chrome-60-deprecations) shipped in July 2017 has already made the change, the compatibility risk should be low.
