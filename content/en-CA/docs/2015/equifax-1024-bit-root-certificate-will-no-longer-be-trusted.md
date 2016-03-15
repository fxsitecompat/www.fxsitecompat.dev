---
title: "Equifax 1024-bit root certificate will no longer be trusted"
date: "2015-10-24T22:41:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1156844"
      title: "Bug 1156844 - Turn off Trust bits for Equifax Secure Certificate Authority 1024-bit root certificate"
---
The trust in the *Equifax Secure Certificate Authority* 1024-bit root certificate, once disabled but [re-enabled in Firefox 38](https://www.fxsitecompat.com/en-CA/docs/2015/1024-bit-ssl-certificates-are-no-longer-trusted/) due to compatibility issues, will be removed with Firefox 44. If you still have a certificate issued by this CA, replace it as soon as possible, or your site will be blocked by Firefox. This change will be the last step in Mozilla's plan to [phase out root certificates with 1024-bit RSA keys](https://blog.mozilla.org/security/2014/09/08/phasing-out-certificates-with-1024-bit-rsa-keys/).
