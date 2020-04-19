---
title: "TLS CBC-mode ECDSA ciphers have been removed"
date: "2017-03-11T21:42:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1316300"
      title: "Bug 1316300 - Deprecate and remove: TLS CBC-mode ECDSA cipher suites"
---
The support for the rarely-used CBC-mode ECDSA cipher suites in TLS 1.3 has been removed with Firefox 53. [Chrome 56](https://www.chromestatus.com/feature/5740978103123968) has already removed it in this January so that the compatibility risk should be low.
