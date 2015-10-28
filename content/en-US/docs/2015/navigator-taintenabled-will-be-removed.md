---
title: "`navigator.taintEnabled` will be removed"
date: "2015-10-27T22:52:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=679971": "Bug 679971 - remove Navigator.taintEnabled()"
---
The Netscape-derived [`navigator.taintEnabled`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID/taintEnabled) method is just returning `false` in Firefox, but apparently it's used by various sites for browser detection. Do not use it anymore or your site may be broken once it's removed.
