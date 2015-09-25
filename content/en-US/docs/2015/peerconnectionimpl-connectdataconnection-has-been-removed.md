---
title: "`PeerConnectionImpl.connectDataConnection` has been removed"
date: "2015-01-16T09:37:54-05:00"
categories: ["audio-video"]
tags: []
versions: "37"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1110478": "Bug 1110478 – Remove unused remnants of non-standard connectDataConnection from Bug 852908"
---
The non-standard [`PeerConnectionImpl.connectDataConnection`](https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/) method, which has been deprecated and no-op (doing nothing) since Firefox 22, is gone. Developers don't have to use this any more.
