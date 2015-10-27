---
title: "`navigator.plugins` will no longer be enumerable"
date: "2015-10-26T21:49:00-07:00"
categories: ["dom", "plugins", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=757726": "Bug 757726 - disallow enumeration of navigator.plugins"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=934107": "Bug 934107 - [meta] Remove use of plugin enumeration"
---
The value returned by the the [`navigator.plugins`](https://bugzilla.mozilla.org/show_bug.cgi?id=757726) property will be unenumerable in the future to minimize fingerprinting. This change was originally planned for Firefox 28, but has been postponed due to the number of broken sites. Note that Firefox will [drop plug-in support by the end of 2016 except Flash](https://www.fxsitecompat.com/en-US/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/), therefore you should avoid serving plug-in content on your site anyway.
