---
title: "CSP `referrer` directive has been removed"
date: "2018-05-08T17:17:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1302449"
      title: "Bug 1302449 - deprecating the \"referrer\" directive in CSP"
---
The Content Security Policy (CSP) [`referrer`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/referrer) directive, deprecated since [Firefox 52](https://www.fxsitecompat.com/en-CA/docs/2017/csp-referrer-directive-has-been-deprecated/), has been removed with Firefox 62 in favour of the [`Referrer-Policy`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Referrer-Policy) HTTP header. Given that [Chrome 56](https://developers.google.com/web/updates/2016/12/chrome-56-deprecations) shipped in January 2017 has already removed the support, the compatibility risk should be low.
