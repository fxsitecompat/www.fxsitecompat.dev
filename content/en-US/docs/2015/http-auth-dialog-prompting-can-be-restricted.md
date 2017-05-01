---
title: "HTTP auth dialog can be restricted"
date: "2015-04-27T13:17:23-04:00"
categories: ["privacy-security"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=647010": "Bug 647010 - Only present HTTP authentication dialogs if it is the top-level document initiating the auth"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1197944": "Bug 1197944 - The bug 647010 (HTTP authentication from sub-resources) cause some problems. Change the pref to revert the behavior"
---
Firefox 40 introduced an option to block [cross-origin](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) sub-resources from showing [an HTTP 401 basic authentication dialog](https://www.fxsitecompat.com/en-US/docs/2015/http-auth-dialog-can-no-longer-be-triggered-by-cross-origin-resources/). In response to the feedback from users this change was [backed out](https://bugzilla.mozilla.org/show_bug.cgi?id=1197944) and by default the authentication is allowed.

The authentication of the sub-resources can be restricted with the hidden `network.auth.subresource-http-auth-allow` preference if needed; see [`all.js`](https://mxr.mozilla.org/mozilla-central/source/modules/libpref/init/all.js#1786) for the possible values.
