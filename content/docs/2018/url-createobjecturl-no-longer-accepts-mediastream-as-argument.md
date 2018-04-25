---
title: "`URL.createObjectURL()` no longer accepts `MediaStream` as argument"
date: "2018-04-24T19:23:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1454889"
      title: "Bug 1454889 - Remove createObjectURL()'s MediaStream overload"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o_0RoYoCmM4/discussion"
      title: "Intent to unship: URL.createObjectURL(MediaStream)"
---
As of Firefox 61, the [`URL.createObjectURL`](https://developer.mozilla.org/en-US/docs/Web/API/URL/createObjectURL) static method no longer accepts a [`MediaStream`](https://developer.mozilla.org/en-US/docs/Web/API/MediaStream) object as the argument. According to the current specs, only a `Blob` or `MediaSource` object can be accepted.

The stream argument support has been [deprecated since Firefox 54](https://www.fxsitecompat.com/en-CA/docs/2017/url-createobjecturl-stream-has-been-deprecated/). [Safari](https://bugs.webkit.org/show_bug.cgi?id=167518) has already made the change, and [Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=800767) may also follow soon.

Whenever you want to set a `MediaStream` object on a `<video>` or `<audio>` element, the [`HTMLMediaElement.prototype.srcObject`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/srcObject) property should be used instead as below:

```js
// This no longer works
video.src = URL.createObjectURL(stream);
// Instead, do this
video.srcObject = stream;
```
