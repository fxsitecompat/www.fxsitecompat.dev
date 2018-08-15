---
title: "`RTCRTPStreamStats.isRemote` has been deprecated"
date: "2018-08-14T20:27:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1393306"
      title: "Bug 1393306 - Add deprecation warning for removal of stat.isRemote in 65."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/kqlQzADXbng/discussion"
      title: "Intent to remove: isRemote member in WebRTC getStats() results"
---
The `isRemote` boolean member of the `RTCRTPStreamStats` dictionary, returned from the `RTCPeerConnection.prototype.getStats` method for remote statistics, is now considered deprecated and will be removed with Firefox 65. Use `remoteId` instead as described in the [WebRTC team's blog post](https://blog.mozilla.org/webrtc/getstats-isremote-65/).
