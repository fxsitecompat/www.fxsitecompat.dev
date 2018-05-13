---
title: "`RTCDataChannel.stream` has been removed"
date: "2016-06-24T14:06:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=878945"
      title: "Bug 878945 - Update DataChannel WebIDL to match spec changes (renaming dictionary values)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1281150"
      title: "Bug 1281150 - Remove obsolete RTCDataChannel.stream property"
---
The [`RTCDataChannel.prototype.stream`](https://developer.mozilla.org/docs/Web/API/RTCDataChannel/stream) property, deprecated since Firefox 22 due to spec changes, is no longer available in Firefox 50 and later. Use the standardized [`id`](https://developer.mozilla.org/docs/Web/API/RTCDataChannel/id) property instead.
