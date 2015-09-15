---
title: "SSLv3 has been disabled"
date: "2014-09-01T22:12:15-04:00"
categories: ["privacy-security"]
tags: []
versions: "34"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1030963": "Bug 1030963 – (POODLE) Padding oracle attack on SSL 3.0"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1085138": "Bug 1085138 – (POODLEBITE) [META] Sites broken due to reliance on a security protocol that was obsolete last millennium"
---
In response to the POODLE attack reported by Google, SSL version 3.0 has been disabled by default in Firefox 34 (Beta 3 and later). [Firefox ESR](https://www.mozilla.org/en-US/firefox/organizations/) for organizations will also disable SSLv3 in the version 31.3.0. According to a comment in the bug, approximately 1% of the Alexa top 1 million domains will be affected by this change due to their SSLv3 requirements. Sites require SSLv3 should upgrade to a recent version of TLS as soon as possible. See the [Mozilla Security Blog](https://blog.mozilla.org/security/2014/10/14/the-poodle-attack-and-the-end-of-ssl-3-0/) for details. Please report affected sites as the [blockers of Bug 1085138](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1085138).
