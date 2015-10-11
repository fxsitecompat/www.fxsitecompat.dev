---
title: "MD5 certificates are no longer accepted"
date: "2012-10-09T06:00:00-04:00"
categories: ["privacy-security"]
tags: []
versions: "16"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=650355": "Bug 650355 – Stop accepting MD5 as a hash algorithm in signatures (toggle security.enable_md5_signatures to false)"
---
The MD5 hash algorithm has been disabled with Firefox 16 because it's [not secure](https://developer.mozilla.org/en-US/docs/Web/Security/Weak_Signature_Algorithm). Firefox users will see an error message when they try to browse a site using a SSL certificate signed with the MD5 algorithm. For the sake of convenience, users still be able to [ignore that error](https://bugzilla.mozilla.org/show_bug.cgi?id=758314).
