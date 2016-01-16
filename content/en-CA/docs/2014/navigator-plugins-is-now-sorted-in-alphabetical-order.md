---
title: "`navigator.plugins` is now sorted in alphabetical order"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["34"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=793978": "Bug 793978 – Sort navigator.plugins array to avoid exposing user-identifying plugin file order"
---
The [`navigator.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/navigator.plugins) array was previously being sorted by the last modified time of installed plug-ins. This could be used by user-tracking softwares to fingerprint users in combination with other characteristics, because even if two users had the same plugin set, the installed order would likely be unique. Starting with Firefox 34, the array is sorted by the plugin's name in alphabetical order to mitigate such a fingerprinting risk.
