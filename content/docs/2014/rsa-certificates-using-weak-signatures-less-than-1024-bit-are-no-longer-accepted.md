---
title: "RSA certificates using weak signatures less than 1024-bit are no longer accepted"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: ["33"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=360126"
      title: "Bug 360126 – Stop accepting certificates that use RSA 1023 or weaker signatures"
---
RSA 512, 1000 and 1023-bit certificates are now blocked by Firefox since they are not sufficient for security. Most certificates currently being issued should have a 2048-bit key length.
