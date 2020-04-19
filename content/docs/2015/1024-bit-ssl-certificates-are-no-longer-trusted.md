---
title: "1024-bit SSL certificates are no longer trusted"
date: "2015-02-27T04:21:22-05:00"
categories: ["privacy-security"]
tags: []
versions: ["38", "38-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881553"
      title: "Bug 881553 - Remove or turn off trust bits for 1024-bit root certs after December 31, 2013"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=936105"
      title: "Bug 936105 - Remove or turn off trust bits for Symantec 1024-bit root certs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=986019"
      title: "Bug 986019 - Turn off SSL and Code Signing trust bits for Equifax 1024-bit roots"
---
The third and final phase of [phasing out 1024-bit root certificates](https://blog.mozilla.org/security/2014/09/08/phasing-out-certificates-with-1024-bit-rsa-keys/) has completed with Firefox 38. As the blog post describes, if your SSL certificate has a 1024-bit key or was issued by a CA with a 1024-bit key, you have to get a new SSL certificate and update it on your Web server.

**Update**: *Equifax Secure Certificate Authority* 1024-bit root has been [temporarily re-enabled](https://bugzilla.mozilla.org/show_bug.cgi?id=1155279) due to considerable breakages.
