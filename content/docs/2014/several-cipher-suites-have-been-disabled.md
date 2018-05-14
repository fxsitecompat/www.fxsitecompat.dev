---
title: "Several cipher suites have been disabled"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: ["33"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1036765"
      title: "Bug 1036765 – Disable cipher suites that are not in the \"Browser Cipher Suite\" proposal that are still enabled"
---
Some obsolete, insecure or little-used cipher suites have been deprecated and disabled by default to match the [cipher suite proposal](https://groups.google.com/d/topic/mozilla.dev.tech.crypto/duNhREcIAe8). Those include 3DES, Camellia, DSS and RC4.
