---
title: "CSP directives with sources containing capital letters are not applied"
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
versions: "35"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1122445": "Bug 1122445 – CSP change in behavior regards case sensitivity loading resources"
---
On Firefox 35, [Content Security Policy (CSP)](https://developer.mozilla.org/en-US/docs/Web/Security/CSP) directives are not applied properly if the source URLs contain capital letters, like `https://www.example.com/OnlineBanking`. Mozilla developers have found that Firefox's current CSP implementation is internally decapitalizing source URLs and therefore they don't match the actual URLs. This issue has been fixed with Firefox 35.0.1.
