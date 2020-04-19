---
title: "Certificate verification backend has been overhauled"
date: "2014-04-03T19:31:02-04:00"
categories: ["privacy-security"]
tags: []
releases: ["31", "31-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=915930"
      title: "Bug 915930 – Make mozilla::pkix the default certificate verifier"
---
The new certificate verification library called mozilla::pkix has been landed on Firefox 31. See [Camilo Viecco's blog post](https://blog.mozilla.org/security/2014/04/24/exciting-updates-to-certificate-verification-in-gecko/) for details. If you encountered any regressions, please [report the issue](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Security%3A%20PSM) to Bugzilla.
