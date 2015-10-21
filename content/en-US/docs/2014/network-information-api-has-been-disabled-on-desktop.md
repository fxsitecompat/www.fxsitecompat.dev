---
title: "Network Information API has been disabled on desktop"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1020758": "Bug 1012944 – [Network Information API] Disable the API on desktop"
---
The [Network Information API](https://developer.mozilla.org/en-US/docs/Web/API/Network_Information_API), implemented as `navigator.mozConnection`, has been disabled on the desktop versions of Firefox since it has been accidentally exposed. Currently the API only works on Firefox for Android and Firefox OS.
