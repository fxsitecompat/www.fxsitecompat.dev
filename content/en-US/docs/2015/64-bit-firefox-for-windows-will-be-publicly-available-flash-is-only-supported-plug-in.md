---
title: "64-bit Firefox for Windows will be publicly available, Flash is only supported plug-in"
date: "2015-06-13T15:20:46-04:00"
categories: ["plugins"]
tags: []
versions: ["43"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1180792": "Bug 1180792 - enable 64-bit windows builds on release channel"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1229852": "Bug 1229852 - Add Firefox Win64 download to /firefox/all/"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1165981": "Bug 1165981 - Whitelist Flash for NPAPI on 64 bit Firefox on Win64"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1187005": "Bug 1187005 - Some plugins (Microsoft Silverlight, Java,...) are not recognized as installed with Firefox 64-bit build on Win64"
aliases:
    - "/docs/2015/64-bit-firefox-for-windows-is-publicly-available-only-flash-is-supported/"
---
Firefox 64-bit builds for Windows have been available for testing as [Developer Edition](https://www.mozilla.org/en-US/firefox/developer/all/) and [Beta](https://www.mozilla.org/en-US/firefox/beta/all/) for a while, and starting with Firefox 42, the 64-bit builds are available to the public via the Release (stable) channel. This means a lot more users will start using the 64-bit version, and if your content requires a 32-bit [NPAPI plug-in](https://developer.mozilla.org/en-US/Add-ons/Plugins), it won't work for those Firefox users. Currently Adobe Flash Player is the only supported plug-in on the 64-bit builds. Content publishers are strongly encouraged to move away from plug-in dependencies in favor of the [latest Web technologies](https://developer.mozilla.org/en-US/docs/Web).

**Update**: The public release of Windows 64-bit builds has been postponed while Mozilla is "waiting for some partner changes". The current timeline is unknown.

**Update**: Mozilla has decided to ship the 64-bit version with Firefox 43.
