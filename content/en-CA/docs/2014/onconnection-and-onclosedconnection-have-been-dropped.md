---
title: "`onconnection` and `onclosedconnection` have been dropped"
date: "2014-06-09T02:46:54-04:00"
categories: ["audio-video"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1014304": "Bug 1014304 – Remove onconnection and onclosedconnection from PC"
---
The `onconnection` and `onclosedconnection` properties have been removed from the [`RTCPeerConnection`](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection) interface, currently implemented as `mozRTCPeerConnection`, since they are no longer in the spec.
