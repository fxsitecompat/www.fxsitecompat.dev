---
title: "Gecko build date in the UA string has been replaced with the version number"
date: "2012-12-03T03:50:54-05:00"
categories: ["networking"]
tags: []
versions: "17"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=588909": "Bug 588909 – Replace Gecko/<date> with Gecko/<version> in UA string"
---
The notation of [Gecko](https://developer.mozilla.org/en-US/docs/Mozilla/Gecko), the rendering engine of Firefox, in the user agent (UA) string has been changed. The build date, that has been fixed since [Firefox 4](https://hacks.mozilla.org/2010/09/final-user-agent-string-for-firefox-4/), was replaced with the version number. Thus `Gecko/20100101` will be `Gecko/17.0`. You should be careful if you're detecting browser version from UA strings.

<ins datetime="2012-11-30">Update on Nov 30: [This change has been backed out from Firefox 17.0.1](https://bugzilla.mozilla.org/show_bug.cgi?id=815743) as it may have a major impact on site compatibility.</ins>
