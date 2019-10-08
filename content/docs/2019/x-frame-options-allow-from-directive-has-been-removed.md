---
title: "`X-Frame-Options: Allow-From` directive has been removed"
date: "2019-10-08T17:17:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1301529"
      title: "Bug 1301529 - Misleading console message for X-Frame-Options Allow-From mismatch (remove X-Frame-Options: allow-from)"
---
The support for the `allow-from` directive for the obsolete [`X-Frame-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Frame-Options) HTTP response header has been dropped with Firefox 70. While it's still useful for older browsers including Internet Explorer, you should be using the `Content-Security-Policy` (CSP) header's [`frame-ancestors`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors) directive in combination for modern browsers.
