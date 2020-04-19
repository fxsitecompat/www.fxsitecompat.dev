---
title: "Deprecated `RTCPeerConnection` functionalities have been removed"
date: "2013-10-08T20:15:35-04:00"
categories: ["audio-video"]
tags: []
releases: ["27", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=929530"
      title: "Bug 929530 – Remove deprecated peerConnection functionality which has produced web console warnings since 24."
---
Some non-standard functionalities deprecated since Firefox 24 have been removed from the (currently prefixed) [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) interface. Those include the `localStreams`, `remoteStreams`, `readyState`, `onicechange` and `ongatheringchange` attributes, as well as calling `createAnswer` or `createOffer` without `failureCallback`.
