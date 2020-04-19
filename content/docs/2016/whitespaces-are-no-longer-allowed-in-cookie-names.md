---
title: "Whitespaces are no longer allowed in cookie names"
date: "2016-01-31T02:11:00-05:00"
categories: ["javascript", "networking"]
tags: []
releases: ["44"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244505"
      title: "Bug 1244505 - Firefox 44 no longer allows spaces in cookie names, breaking some apps"
    - url: "https://www.mozilla.org/security/advisories/mfsa2016-04/"
      title: "MFSA 2016-04 - Firefox allows for control characters to be set in cookie names"
---
Previously, Firefox was improperly allowing whitespace characters to be stored in cookie names in violation of RFC 6265. This behaviour was considered as a moderate security issue, because such an implementation error could lead to incorrect cookie handling by Web servers.

Firefox 44 has fixed the issue and cookies with an invalid name are no longer created. In JavaScript, both cookie names and values must be explicitly encoded using the [`encodeURIComponent`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent) method before being stored with the [`document.cookie`](https://developer.mozilla.org/docs/Web/API/Document/cookie) property.

**Update**: Due to some broken applications, this change has been reverted with Firefox 44.0.1. While spaces are allowed again for interoperability, control characters will remain prohibited to prevent potential security issues.
