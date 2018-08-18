---
title: "Symantec, GeoTrust, RapidSSL, Thawte, Verisign certificates will all be distrusted in October 2018"
date: "2018-06-05T12:53:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["63"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460062"
      title: "Bug 1460062 - Enforce Symantec distrust in Firefox 63"
    - url: "https://blog.mozilla.org/security/2018/03/12/distrust-symantec-tls-certificates/"
      title: "Mozilla Security Blog: Distrust of Symantec TLS Certificates"
    - url: "https://blog.mozilla.org/security/2018/07/30/update-on-the-distrust-of-symantec-tls-certificates/"
      title: "Update on the Distrust of Symantec TLS Certificates"
---
As the last step in the ongoing multi-vendor distrust actions against Symantec due to the [various CA practice issues](https://wiki.mozilla.org/CA:Symantec_Issues), Firefox 63 shipping October 23 will remove the trust in all the existing TLS server certificates issued by Symantec, including ones issued under the GeoTrust, RapidSSL, Thawte and Verisign brands. The same change will be made to [Google Chrome 70](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html) shipping October 16.

[Firefox 58](https://www.fxsitecompat.com/en-CA/docs/2018/symantec-issued-certificates-will-soon-be-distrusted/) and later have shown a console warning for the affected certificates, and [Firefox 60](https://www.fxsitecompat.com/en-CA/docs/2018/symantec-certificates-issued-before-june-2016-are-now-distrusted/) has already distrusted ones issued before June 2016. Firefox 63 and later will show the Insecure Connection error page for sites using a Symantec-issued certificate regardless of the issue date.

To avoid the unwanted error page, webmasters using any of these certificates have to [replace it with a new one](https://www.symantec.com/connect/blogs/information-replacement-symantec-ssltls-certificates) or obtain an alternative certificate from other CA as soon as possible. We recommend [Let's Encrypt](https://letsencrypt.org/) that offers trusted certificates for free.

**Update**: The change has been made to [Firefox Nightly](https://blog.nightly.mozilla.org/2018/08/14/symantec-distrust-in-firefox-nightly-63/) on August 14, and affected sites are being tracked in [Bug 1484006](https://bugzilla.mozilla.org/show_bug.cgi?id=1484006).
