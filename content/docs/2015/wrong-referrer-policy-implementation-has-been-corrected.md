---
title: "Wrong Referrer Policy implementation has been corrected"
date: "2015-09-21T21:07:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["41"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1163743"
      title: "Bug 1163743 - (referrer policy) origin-when-crossorigin should have a hyphen in cross-origin"
---
Firefox, along with Google Chrome, was implementing a wrong policy value, `origin-when-crossorigin`, found in the [Referrer Policy specification](https://w3c.github.io/webappsec/specs/referrer-policy/), since the support for [`<meta name="referrer">`](https://developer.mozilla.org/docs/Web/HTML/Element/meta#attr-name) and the [CSP 1.1 `referrer` directive](https://developer.mozilla.org/docs/Web/Security/CSP/CSP_policy_directives#referrer) has been added to Firefox 36 and 37 respectively. The spec has been updated and Firefox 41 has added the support for the correct value, `origin-when-cross-origin` (notice an extra hyphen). The legacy wrong value will no longer be supported in the future.
