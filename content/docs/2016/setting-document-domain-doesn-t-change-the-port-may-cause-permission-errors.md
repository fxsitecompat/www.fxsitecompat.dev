---
title: "Setting `document.domain` doesn't change the port, may cause permission errors"
date: "2016-09-25T01:23:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
releases: ["48"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1292522"
      title: "Bug 1292522 - with document.domain set on iframe/parent, permission denied on property-access across frame/parent when coming from different ports"
---
It's possible to set the [`document.domain`](https://developer.mozilla.org/docs/Web/API/Document/domain) property so that documents from different subdomains, usually a parent page and an `<iframe>` page, can talk to each other. When [changing the origin](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy#Changing_origin) in this way, the port number of the document will be `null`. On Firefox 48, however, the port number is not overwritten, and therefore access between documents on different ports will fail unless they set the same port number with `document.domain`. This regression, causing "permission denied" errors due to a same-origin policy violation, has been fixed with Firefox 49.
