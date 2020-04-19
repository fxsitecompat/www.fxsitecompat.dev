---
title: "CSP directive `frame-src` has been deprecated in favour of `child-src`"
date: "2015-11-17T14:08:00-08:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1045891"
      title: "Bug 1045891 - Implement CSP 1.1 child-src directive"
aliases:
    - "/en-CA/docs/2015/csp-directive-frame-src-has-been-deprecated-in-favor-of-child-src/"
---
The [`frame-src`](https://developer.mozilla.org/docs/Web/Security/CSP/CSP_policy_directives#frame-src) directive of the Content Security Policy (CSP) is now considered deprecated. Use the CSP 1.1 [`child-src`](https://developer.mozilla.org/docs/Web/Security/CSP/CSP_policy_directives#child-src) directive instead while leaving `frame-src` for a while for backward compatibility.
