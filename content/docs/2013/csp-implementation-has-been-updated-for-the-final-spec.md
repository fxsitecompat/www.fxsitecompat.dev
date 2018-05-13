---
title: "CSP implementation has been updated for the final spec"
date: "2013-04-06T04:52:59-04:00"
categories: ["privacy-security"]
tags: []
versions: ["23"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=746978"
      title: "Bug 746978 – sync CSP directive parsing and directive names with w3c CSP 1.0 spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=783049"
      title: "Bug 783049 – CSP : use existing/old parser for X-Content-Security-Policy header, new/CSP 1.0 spec compliant parser for Content-Security-Policy header"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=842657"
      title: "Bug 842657 – Flip the pref to enable the CSP 1.0 parser for Firefox"
---
[Content Security Policy (CSP)](https://developer.mozilla.org/docs/Security/CSP) 1.0 spec has been implemented. The existing parser will be used when a policy is served via the `X-Content-Security-Policy` header, and the new parser that follows the 1.0 spec will be used when a policy is served via the officially spec'd `Content-Security-Policy` header. See the [post on the Mozilla Security Blog](https://blog.mozilla.org/security/2013/06/11/content-security-policy-1-0-lands-in-firefox/) for details. Consult the latest spec if you'd like to implement CSP on your site. The [documents on MDN](https://developer.mozilla.org/docs/Security/CSP) will be updated sometime soon.
