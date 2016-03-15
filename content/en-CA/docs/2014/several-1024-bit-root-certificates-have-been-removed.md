---
title: "Several 1024-bit root certificates have been removed"
date: "2014-06-09T02:46:54-04:00"
categories: ["privacy-security"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881553"
      title: "Bug 881553 – Remove or turn off trust bits for 1024-bit root certs after December 31, 2013"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1029561"
      title: "Bug 1029561 – Update Mozilla 32 to use NSS 3.16.3 after July 1st to include root CA updates"
---
As part of the ongoing security improvements, several SSL and code signing trust bits for 1024-bit root certificates have been removed from [Network Security Services (NSS)](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/NSS) used in Firefox and other products. Those include *AC Raíz Certicámara*, *Entrust.net*, *GTE CyberTrust*, *NetLock*, *TDC Internet*, *ValiCert* and *VeriSign*. [1024-bit root certificates will all be removed](https://wiki.mozilla.org/CA:MD5and1024) over the next few Firefox releases, because these are no longer considered as secure.
