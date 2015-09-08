---
title: "Proxy authentication using cookies doesn\'t work"
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: ["regression"]
versions: "35"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1121895": "Bug 1121895 – Proxy authentication with Auth-Cookies not working anymore"
---
Firefox 35 has fixed a [security bug](https://www.mozilla.org/security/advisories/mfsa2015-04/) that allowed cookie injections using a 407 Proxy Authentication HTTP response. As a side effect, legitimate cookie authentications for corporate intranet sites are no longer working because auth cookies cannot be set by proxy servers. Mozilla developers are discussing how to solve the issue securely. [Firefox 31 ESR](https://www.mozilla.org/firefox/organizations/) is available for enterprise users to workaround the issue.
