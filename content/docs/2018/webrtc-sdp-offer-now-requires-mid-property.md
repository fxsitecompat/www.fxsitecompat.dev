---
title: "WebRTC SDP offer now requires `mid` property"
date: "2018-10-16T10:12:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["63"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1483338"
      title: "Bug 1483338 - Key media transports by a string id rather than level"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1487617"
      title: "Bug 1487617 - Google Meet and Hangouts stopped working in Firefox 63"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1495569"
      title: "Bug 1495569 - Firefox 63 bricks TextNow.com calls"
---
As part of the ongoing WebRTC spec compliance work, Firefox 63 and later will use a string ID ([MID](https://developer.mozilla.org/docs/Web/API/RTCIceCandidate/sdpMid)) instead of an integer level ([m-line index](https://developer.mozilla.org/docs/Web/API/RTCIceCandidate/sdpMLineIndex)) as the identifier for media transports. Because of this, SDP offers should also be spec compliant, requiring the `mid` property. The simplest solution here is adding `a=mid:0` to offers, according to a Mozilla engineer's [bug comment](https://bugzilla.mozilla.org/show_bug.cgi?id=1495569#c17).

*Google Meet* and *Hangouts* were broken after the change was made, but Google has already fixed the issue. *TextNow* is also known to be broken.
