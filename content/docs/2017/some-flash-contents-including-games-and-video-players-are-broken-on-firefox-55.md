---
title: "Some Flash contents including games and video players are broken on Firefox 55"
date: "2017-08-29T19:02:00-04:00"
categories: ["plugins"]
tags: []
versions: ["55", "60-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1340934"
      title: "Bug 1340934 - Re-enable Flash async drawing"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1393352"
      title: "Bug 1393352 - flash player: Font white on white background"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1394105"
      title: "Bug 1394105 - Firefox 55 - performance of Shockwave Flash content has dropped significantly, with web based flash running very slowly, disabling async drawing solves the issue"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1394408"
      title: "Bug 1394408 - [meta] tab switching bugs related to async painting"
---
Firefox 55 for Windows has enabled the async drawing of Flash plug-in content. While this change generally improves the browser performance, there are several regressions including text becoming white, performance declining significantly, and response aborting when switching tabs. Not all Flash sites and users are affected, and some people have already solved their issue by [enabling Flash hardware acceleration](https://forums.adobe.com/thread/891337). Also, the Windows 64-bit version of Firefox is likely unaffected. Mozilla developers are investigating the root cause.

**Update**: Mozilla developers are looking at the painting issue on tab switch. Other bugs are being investigated by Adobe.
