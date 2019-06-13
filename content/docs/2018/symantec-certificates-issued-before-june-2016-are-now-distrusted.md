---
title: "Symantec certificates issued before June 2016 are now distrusted"
date: "2018-03-12T14:12:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["60"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1434300"
      title: "Bug 1434300 - Distrust Symantec CAs affected by the distrust plan"
---
Firefox 60 shipping on May 9 will distrust TLS server certificates issued by Symantec prior to June 1, 2016, which have been announced as [deprecated since Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2018/symantec-issued-certificates-will-soon-be-distrusted/). Google Chrome 66 shipping on April 17 is going to make the [same change](https://security.googleblog.com/2017/09/chromes-plan-to-distrust-symantec.html). All the Symantec brands including GeoTrust, RapidSSL, Thawte and Verisign will be affected by the multi-vendor distrust actions due to a [number of CA practice issues](https://wiki.mozilla.org/CA:Symantec_Issues).

To avoid unwanted Insecure Connection error pages, webmasters using any Symantec-issued certificate, particularly on [this top site list](https://bugzilla.mozilla.org/attachment.cgi?id=8953758), have to [replace it with a new one](https://www.symantec.com/connect/blogs/information-replacement-symantec-ssltls-certificates) or obtain an alternative certificate from other CA as soon as possible. We recommend [Let's Encrypt](https://letsencrypt.org/) that offers trusted certificates for free.

Firefox 63 and Chrome 70, both shipping in October, will distrust all Symantec certificates regardless of the issue date.
