---
title: "`token` has been removed from `RTCIceCredentialType`"
date: "2019-06-09T05:25:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1529595"
      title: "Bug 1529595 - Remove \"token\" from RTCIceCredentialType"
---
The `token` constant has been removed from the `RTCIceCredentialType` enum, which is used for the [`RTCIceServer.prototype.credentialType`](https://developer.mozilla.org/docs/Web/API/RTCIceServer/credentialType) property, according to the current WebRTC 1.0 spec. Given that `oauth` added to the spec is not yet supported in Firefox, only `password` can be used at this time.
