---
title: "Wildcard in CSP policy directives no longer allows `blob:`, `data:` and `filesystem:` resources"
date: "2015-04-27T13:17:23-04:00"
categories: ["privacy-security"]
tags: []
versions: ["40"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1086999": "Bug 1086999 - CSP: Asterisk (*) wildcard should not allow blob:, data:, or filesystem: when matching source expressions"
    "https://www.mozilla.org/en-US/security/advisories/mfsa2015-91/": "MFSA 2015-91 - Mozilla Content Security Policy allows for asterisk wildcards in violation of CSP specification"
---
Firefox was incorrectly allowing resources from the `blob:`, `data:` and `filesystem:` URLs when an asterisk wildcard (`*`) was used in [CSP policy directives](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/CSP_policy_directives). This behavior has been fixed with Firefox 40. So far, [*CNN*](https://bugzilla.mozilla.org/show_bug.cgi?id=1155792), [*Facebook*](https://bugzilla.mozilla.org/show_bug.cgi?id=1181379), [*FastMail*](https://bugzilla.mozilla.org/show_bug.cgi?id=1157084) and [*WhatsApp*](https://bugzilla.mozilla.org/show_bug.cgi?id=1154704) are known to be affected from this change, because those sites have `img-src: *` in their directives while using `data:` URLs to show images. The solution of this is explicitly adding `data:` to the appropriate directive.
