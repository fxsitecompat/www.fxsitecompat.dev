---
title: "`negotiationneeded` event is no longer suppressed before the first offer"
date: "2015-04-27T13:17:23-04:00"
categories: ["audio-video"]
tags: []
versions: "40"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1149838": "Bug 1149838 - We should not suppress negotiationneeded before the first offer/answer exchange"
---
The [`negotiationneeded`](https://developer.mozilla.org/en-US/docs/Web/Events/negotiationneeded) event is now properly fired even before the first offer/answer exchange. If you are expecting the event to be called only for re-negotiations, please review your code to avoid any unexpected errors.
