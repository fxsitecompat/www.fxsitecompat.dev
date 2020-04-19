---
title: "`onconnection` and `onclosedconnection` have been dropped"
date: "2014-06-09T02:46:54-04:00"
categories: ["audio-video"]
tags: []
versions: ["32", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1014304"
      title: "Bug 1014304 – Remove onconnection and onclosedconnection from PC"
---
The `onconnection` and `onclosedconnection` properties have been removed from the [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) interface, currently implemented as `mozRTCPeerConnection`, since they are no longer in the spec.
