---
title: "Some `RTCPeerConnection` methods soon require callbacks"
date: "2014-10-17T22:50:44-04:00"
categories: ["audio-video"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1064088"
      title: "Bug 1064088 – PeerConnection should log deprecation warnings when required callbacks are missing."
---
The [`setLocalDescription`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection.setLocalDescription), [`setRemoteDescription`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection.setRemoteDescription) and [`addIceCandidate`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection.addIceCandidate) methods on the [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) interface can have a success callback and an error callback as the arguments. Firefox 32 required these callback arguments according to the updated spec, but the change has been reverted with Firefox 32.0.1 due to a [site compatibility issue](https://bugzilla.mozilla.org/show_bug.cgi?id=1063971). The callbacks will be required again in the future, so the [Web Console](https://developer.mozilla.org/docs/Tools/Web_Console) has started to show a deprecation warning if callbacks are missing.
