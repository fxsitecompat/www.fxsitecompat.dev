---
title: "`MediaStream.stop()` has been deprecated"
date: "2015-10-01T16:06:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1103188"
      title: "Bug 1103188 - Implement MediaStream.addTrack()/removeTrack()"
---
The `stop` method on the [`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) interface has been removed from the WebRTC specification and deprecated in Firefox 44. To stop a streaming, use the [`MediaStreamTrack.stop`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack/stop) method instead as the following code snippet shows.

```js
navigator.mediaDevices.getUserMedia({
  audio: false,
  video: true
}).then(stream => {
  // stream.stop(); // Deprecated
  stream.getVideoTracks()[0].stop(); // Recommended
});
```

[According to the developer](https://bugzilla.mozilla.org/show_bug.cgi?id=1103188#c106), there will be a couple more changes to the WebRTC implementation to comply with the latest spec. We will document any changes affecting backward compatibility.
