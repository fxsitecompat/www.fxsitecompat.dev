---
title: "64-bit Firefox for Windows is officially available, Flash and Silverlight are the only supported plug-ins"
date: "2015-06-13T15:20:46-04:00"
categories: ["plugins"]
tags: []
versions: ["43"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1180792"
      title: "Bug 1180792 - enable 64-bit windows builds on release channel"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1229852"
      title: "Bug 1229852 - Add Firefox Win64 download to /firefox/all/"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165981"
      title: "Bug 1165981 - Whitelist Flash for NPAPI on 64 bit Firefox on Win64"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1225293"
      title: "Bug 1225293 - Support Silverlight for Win64 Firefox"
aliases:
    - "/docs/2015/64-bit-firefox-for-windows-is-publicly-available-only-flash-is-supported/"
    - "/docs/2015/64-bit-firefox-for-windows-will-be-publicly-available-flash-is-only-supported-plug-in/"
---
Firefox 64-bit builds for Windows have been available for testing as [Developer Edition](https://www.mozilla.org/en-US/firefox/developer/all/) and [Beta](https://www.mozilla.org/en-US/firefox/beta/all/) for a while, and starting with Firefox 42, the 64-bit builds are available to the public via the [Release](https://www.mozilla.org/en-US/firefox/all/) (stable) channel. This means a lot more users will start using the 64-bit version, and if your content requires a 32-bit [NPAPI plug-in](https://developer.mozilla.org/en-US/Add-ons/Plugins), it won't work for those Firefox users. Currently Adobe Flash Player is the only supported plug-in on the 64-bit builds. Content publishers are strongly encouraged to move away from plug-in dependencies in favour of the [latest Web technologies](https://developer.mozilla.org/en-US/docs/Web).

**Update**: The public release of Windows 64-bit builds has been postponed while Mozilla is "waiting for some partner changes". The current timeline is unknown.

**Update**: Mozilla has decided to ship the 64-bit version with Firefox 43, enabling the Silverlight support as well.

**Update**: There is a [bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1236911) on 64-bit builds where the file picker cannot be opened from Flash content. Mozilla is working with Adobe to solve the issue.
