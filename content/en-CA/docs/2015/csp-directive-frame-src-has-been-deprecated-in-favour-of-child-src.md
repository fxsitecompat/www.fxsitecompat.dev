---
title: "CSP directive `frame-src` has been deprecated in favour of `child-src`"
date: "2015-11-17T14:08:00-08:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1045891"
      title: "Bug 1045891 - Implement CSP 1.1 child-src directive"
aliases:
    - "/docs/2015/csp-directive-frame-src-has-been-deprecated-in-favor-of-child-src/"
---
The [`frame-src`](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/CSP_policy_directives#frame-src) directive of the Content Security Policy (CSP) is currently considered deprecated in favor of the CSP 1.1 [`child-src`](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/CSP_policy_directives#child-src) directive.
It should be noted that `child-src` is currently considered for deprecation in CSP 2.0 and 3, so leaving `frame-src` in place is recommended despite being deprecated.
