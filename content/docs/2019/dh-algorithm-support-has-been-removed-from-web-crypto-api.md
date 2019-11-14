---
title: "DH algorithm support has been removed from Web Crypto API"
date: "2019-11-14T07:33:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1564509"
      title: "Bug 1564509 - Remove support for DH from WebCrypto API (not in spec)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Ut3-eQmUdWg/discussion"
      title: "Intent-to-Unship: DH algorithm support for WebCrypto"
---
Firefox 72 has removed the support for the Diffie–Hellman (DH) key exchange algorithm from the [`SubtleCrypto.generateKey`](https://developer.mozilla.org/docs/Web/API/SubtleCrypto/generateKey) method, because it's not included in the final [Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) spec. Firefox is the only browser supporting the algorithm, and the usage is extremely low according to Mozilla developers, so the compatibility impact should be minimum.
