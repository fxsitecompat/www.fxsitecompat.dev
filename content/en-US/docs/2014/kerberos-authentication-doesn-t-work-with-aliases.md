---
title: "Kerberos authentication doesn\'t work with aliases"
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
versions: "35"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1108971": "Bug 1108971 – Kerberos authentication does not work with alias"
---
Firefox 35 cannot resolve CNAME records (short domain names or aliases) of servers on Kerberos authentication so enterprise users may fail to authenticate against intranet sites or proxy servers with the Kerberos protocol. This issue has been fixed with Firefox 35.0.1. [Firefox 31 ESR](https://www.mozilla.org/firefox/organizations/) is available for enterprise users to workaround the issue.
