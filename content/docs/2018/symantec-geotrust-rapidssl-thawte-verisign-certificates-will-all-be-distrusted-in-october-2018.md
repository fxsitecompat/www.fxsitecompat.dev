---
title: "Symantec, GeoTrust, RapidSSL, Thawte, Verisign certificates will all be distrusted in October 2018"
date: "2018-06-05T12:53:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["64"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460062"
      title: "Bug 1460062 - Enforce Symantec distrust in Firefox 63"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496467"
      title: "Bug 1496467 - Enable Symantec Distrust in Firefox 64 Beta"
    - url: "https://blog.mozilla.org/security/2018/03/12/distrust-symantec-tls-certificates/"
      title: "Mozilla Security Blog: Distrust of Symantec TLS Certificates"
    - url: "https://blog.mozilla.org/security/2018/07/30/update-on-the-distrust-of-symantec-tls-certificates/"
      title: "Update on the Distrust of Symantec TLS Certificates"
---
As the last step in the ongoing multi-vendor distrust actions against Symantec due to the [various CA practice issues](https://wiki.mozilla.org/CA:Symantec_Issues), Firefox 63 shipping October 23 will remove the trust in all the existing TLS server certificates issued by Symantec, including ones issued under the GeoTrust, RapidSSL, Thawte and Verisign brands. The same change will be made to [Google Chrome 70](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html) shipping October 16.

[Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2018/symantec-issued-certificates-will-soon-be-distrusted/) and later have shown a console warning for the affected certificates, and [Firefox 60](https://www.fxsitecompat.dev/en-CA/docs/2018/symantec-certificates-issued-before-june-2016-are-now-distrusted/) has already distrusted ones issued before June 2016. Firefox 63 and later will show the Insecure Connection error page for sites using a Symantec-issued certificate regardless of the issue date.

To avoid the unwanted error page, webmasters using any of these certificates have to [replace it with a new one](https://www.symantec.com/connect/blogs/information-replacement-symantec-ssltls-certificates) or obtain an alternative certificate from other CA as soon as possible. We recommend [Let's Encrypt](https://letsencrypt.org/) that offers trusted certificates for free.

**Update**: The change has been made to [Firefox Nightly](https://blog.nightly.mozilla.org/2018/08/14/symantec-distrust-in-firefox-nightly-63/) on August 14, and affected sites are being tracked in [Bug 1484006](https://bugzilla.mozilla.org/show_bug.cgi?id=1484006). Firefox Beta and Developer Edition will be updated with the change on September 25.

**Update 2**: Given that there are still many affected sites, Firefox 63 Beta 9 shipping September 25 is not enabling the distrust by default. Mozilla engineers are watching the situation closely to decide when they should enable it.

**Update 3**: Mozilla has officially announced that it will [postpone the distrust](https://blog.mozilla.org/security/2018/10/10/delaying-further-symantec-tls-certificate-distrust/) to Firefox 64 Beta shipping in mid-October.

**Update 4**: The distrust is now enabled in Firefox 64 Beta. Webmasters still using one of affected certificates must act now.
