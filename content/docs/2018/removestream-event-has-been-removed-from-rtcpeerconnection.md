---
title: "`removestream` event has been removed from `RTCPeerConnection`"
date: "2018-05-09T09:54:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1442385"
      title: "Bug 1442385 - Remove dead onremovestream code"
---
The [`removestream`](https://developer.mozilla.org/en-US/docs/Web/Events/removestream) event and the corresponding [`onremovestream`](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection/onremovestream) event handler property on the `RTCPeerConnection` interface have been removed with Firefox 60, because these are no longer in the WebRTC spec. The `removetrack` event and the corresponding [`onremovetrack`](https://developer.mozilla.org/en-US/docs/Web/API/MediaStream/onremovetrack) event handler on `MediaStream` should be used instead.
