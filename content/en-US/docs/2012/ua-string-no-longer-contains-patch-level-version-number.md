---
title: "UA string no longer contains patch level version number"
date: "2012-10-09T06:00:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: "16"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=728831": "Bug 728831 – Don’t expose the Firefox patch level (13.X.Y) in the UA string, only show the major version (13.X)"
---
The user agent (UA) string of Firefox no longer exposes the security patch level version number in order to mitigate fingerprinting risks. Therefore, if unscheduled Firefox 16.0.1 is released, the version number in the UA string will just be `16.0` instead of `16.0.1`.
