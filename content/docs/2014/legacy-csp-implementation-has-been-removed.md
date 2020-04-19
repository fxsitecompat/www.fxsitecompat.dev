---
title: "Legacy CSP implementation has been removed"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
releases: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949533"
      title: "Bug 949533 – Remove non-standard CSP parser and X-Content-Security-Policy header support"
---
The legacy, non-standard [Content Security Policy (CSP)](https://developer.mozilla.org/docs/Web/Security/CSP) parser first shipped with Firefox 4 has been removed in favour of the standard CSP 1.0 spec implemented with Firefox 23. The prefixed `X-Content-Security-Policy` header is no longer supported.
