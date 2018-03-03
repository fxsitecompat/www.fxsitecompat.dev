---
title: "`DataChannel` has been renamed to `RTCDataChannel`"
date: "2018-03-03T11:46:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1173851"
      title: "Bug 1173851 - Rename DataChannel to RTCDataChannel per specification"
---
Previously, Firefox was implementing the [`RTCDataChannel`](https://developer.mozilla.org/en-US/docs/Web/API/RTCDataChannel) interface as `DataChannel` so WebRTC feature detection with it could have failed. This wrong name has been corrected with Firefox 60 to comply with the spec. Given that both Chrome and Safari implement the interface as the correct name, the compatibility risk should be low.
