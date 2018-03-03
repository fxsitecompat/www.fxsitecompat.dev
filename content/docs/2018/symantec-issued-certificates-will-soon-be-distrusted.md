---
title: "Symantec-issued certificates will soon be distrusted"
date: "2018-03-02T21:48:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["58"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1409259"
      title: "Bug 1409259 - Implement a console warning for Symantec CAs affected by the distrust plan"
---
Mozilla, among multiple browser vendors, has decided to distrust all TLS server certificates issued by Symantec due to the poor CA practice found through an [extensive investigation](https://wiki.mozilla.org/CA:Symantec_Issues) and discussion. The [upcoming distrust actions](https://wiki.mozilla.org/CA/Upcoming_Distrust_Actions) in Firefox keeps in line with [Google Chrome](https://security.googleblog.com/2017/09/chromes-plan-to-distrust-symantec.html) and applies to all the Symantec brands including GeoTrust, RapidSSL, Thawte and Verisign.

* Firefox 60 shipping on May 9, 2018 shows the Insecure Connection error page for sites using a Symantec certificate issued before June 2016
* Firefox 63 shipping on October 16, 2018 removes all the Symantec root certificates, shows the Insecure Connection error page for sites using a Symantec certificate regardless of the issue date

Before these dates, webmasters using any Symantec-issued certificate have to [replace it with a new one](https://www.symantec.com/connect/blogs/information-replacement-symantec-ssltls-certificates) or obtain an alternative certificate from any other CA such as [Let's Encrypt](https://letsencrypt.org/). Firefox 58 and 59 will show a console warning for sites using a Symantec certificate to encourage the migration.
