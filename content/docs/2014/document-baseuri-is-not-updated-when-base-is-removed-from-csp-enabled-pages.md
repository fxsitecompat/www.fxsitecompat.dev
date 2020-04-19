---
title: "`document.baseURI` is not updated when `<base>` is removed from CSP-enabled pages"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
releases: ["35"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1121857"
      title: "Bug 1121857 – document.baseURI does not get updated to document.location after base tag is removed from DOM for site with a CSP"
---
The [`<base>`](https://developer.mozilla.org/docs/Web/HTML/Element/base) element can be used to change the [`Node.baseURI`](https://developer.mozilla.org/docs/Web/API/Node.baseURI) property's value. When the element is removed, `baseURI` should be automatically reverted to the default value, which is [`document.location`](https://developer.mozilla.org/docs/Web/API/document.location), but the restoration doesn't work on Firefox 35 if [CSP (Content Security Policy)](https://developer.mozilla.org/docs/Web/Security/CSP) is enabled for the document. This issue has been fixed with Firefox 35.0.1.
