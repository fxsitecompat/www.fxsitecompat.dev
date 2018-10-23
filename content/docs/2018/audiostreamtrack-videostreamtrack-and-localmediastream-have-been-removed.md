---
title: "`AudioStreamTrack`, `VideoStreamTrack` and `LocalMediaStream` have been removed"
date: "2018-10-23T02:50:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1258143"
      title: "Bug 1258143 - Remove LocalMediaStream (and its Stop()) from js"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1377146"
      title: "Bug 1377146 - Remove AudioStreamTrack and VideoStreamTrack"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dPyxsKABnKY/discussion"
      title: "Intent to unship: AudioStreamTrack and VideoStreamTrack"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/mA200p2N-Hk/discussion"
      title: "Intent to unship: LocalMediaStream"
---
The `AudioStreamTrack` and `VideoStreamTrack` interfaces, subclasses of [`MediaStreamTrack`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack), have been removed with Firefox 64. Firefox was the only browser supporting these legacy interfaces removed from the Media Capture and Streams spec back in 2014. If necessary, the type of a `MediaStreamTrack` object can be detected using the [`kind`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack/kind) property.

The [`LocalMediaStream`](https://developer.mozilla.org/docs/Web/API/LocalMediaStream) interface has also been removed. The [`getUserMedia`](https://developer.mozilla.org/docs/Web/API/MediaDevices/getUserMedia) method now returns a [`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) object instead of `LocalMediaStream`, which was implemented only in Firefox. Its `stop` method [deprecated since Firefox 44](https://www.fxsitecompat.com/en-CA/docs/2015/mediastream-stop-has-been-deprecated/) can be replaced with the [`stop`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack/stop) method on the `MediaStreamTrack` interface, as shown below:

```js
navigator.mediaDevices.getUserMedia({
  audio: false,
  video: true
}).then(stream => {
  // Instead of stream.stop(), do this:
  stream.getVideoTracks()[0].stop();
});
```
