---
title: "`navigator.platform` now returns `Win32` even on 64-bit Firefox"
date: "2018-08-14T03:35:00-04:00"
categories: ["dom", "html"]
tags: []
versions: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1472618"
      title: "Bug 1472618 - navigator.platform returns \"Win64\" in Firefox on Win64 OS but \"Win32\" in Chrome and Edge"
---
Starting with Firefox 63, the [`navigator.platform`](https://developer.mozilla.org/docs/Web/API/NavigatorID/platform) property will return `"Win32"` on all Windows platforms, even on the 64-bit version of Firefox. This change has been made to avoid potential web compatibility issues, given that both 64-bit Google Chrome and 64-bit Microsoft Edge are returning `"Win32"` on purpose. Meanwhile, `navigator.oscpu` and `navigator.userAgent` will continue revealing the real platform.
