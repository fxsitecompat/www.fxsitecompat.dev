---
title: "SSLv3 support has been removed"
date: "2015-03-17T14:02:59-04:00"
categories: ["privacy-security"]
tags: []
versions: ["39"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1106470": "Bug 1106470 - Drop SSLv3 support entirely"
    "https://groups.google.com/d/topic/mozilla.dev.platform/9hb0mzlHpks/discussion": "Intent to and unship: SSLv3"
---
The SSL 3.0 support in the Mozilla products, [disabled since Firefox 34](https://www.fxsitecompat.com/en-US/docs/2014/sslv3-has-been-disabled/), has been completely dropped because [the protocol is no longer secure](https://blog.mozilla.org/security/2014/10/14/the-poodle-attack-and-the-end-of-ssl-3-0/). Web sites should adopt TLS 1.2 instead.
