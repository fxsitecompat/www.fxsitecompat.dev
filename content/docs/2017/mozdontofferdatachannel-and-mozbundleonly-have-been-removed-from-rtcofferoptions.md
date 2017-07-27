---
title: "`mozDontOfferDataChannel` and `mozBundleOnly` have been removed from `RTCOfferOptions`"
date: "2017-07-20T13:08:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["56"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1196974"
      title: "Bug 1196974 - Remove mozDontOfferDataChannel/mozBundleOnly from RTCOfferOptions"
---
The non-standard, undocumented `mozDontOfferDataChannel` and `mozBundleOnly` boolean attributes have been removed from the `RTCOfferOptions` dictionary. These options could be used for the [`RTCPeerConnection.prototype.createOffer`](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection/createOffer) method.
