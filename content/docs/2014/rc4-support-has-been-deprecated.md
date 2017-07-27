---
title: "RC4 support has been deprecated"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: ["36"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=947149"
      title: "Bug 947149 – Connection information claims RC4 is \"high grade\""
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=999544"
      title: "Bug 999544 – RC4 Considered Harmful: Proposal to disable use of RC4 completely"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1088915"
      title: "Bug 1088915 – Stop offering RC4 in the first handshakes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1093595"
      title: "Bug 1093595 – Treat SSL3 and RC4 as broken"
---
The RC4 cipher suites are now considered insecure. RC4 is no longer offered in the first TLS handshakes, and the security UI in Firefox no longer calls it "high-grade encryption" but rather would say "encryption is not strong enough". The RC4 support will completely be removed from Mozilla products in the near future. Webmasters should upgrade their servers as soon as possible to utlize stronger cipher suites.

**Update**: The RC4 support has been [disabled with Firefox 44](https://www.fxsitecompat.com/en-CA/docs/2015/rc4-is-now-completely-disabled-by-default/).
