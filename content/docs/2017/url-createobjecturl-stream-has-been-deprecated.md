---
title: "`URL.createObjectURL(stream)` has been deprecated"
date: "2017-02-02T22:38:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["54"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1334564"
      title: "Bug 1334564 - Deprecate URL.createObjectURL(mediastream)"
---
Firefox and other browsers will soon stop accepting a [`MediaStream`](https://developer.mozilla.org/en-US/docs/Web/API/MediaStream) as the object argument for the [`URL.createObjectURL`](https://developer.mozilla.org/en-US/docs/Web/API/URL/createObjectURL) static method, as the result of discussions among the developers. Firefox 54 will show a deprecation warning in the console when such code is found.

As an [example in the spec](https://w3c.github.io/mediacapture-main/#examples) demonstrates, the [`HTMLMediaElement.prototype.srcObject`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/srcObject) property should be used to set a `MediaStream` on a `<video>` or `<audio>` element.

```js
// Don't do this
video.src = URL.createObjectURL(stream);
// Do this
video.srcObject = stream;
```

**Update**: The deprecation warning is not displayed on Firefox 54 due to a [bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1369698). Firefox 55 and later will show it properly.

**Update 2**: The stream argument support has been [removed with Firefox 61](https://www.fxsitecompat.com/en-CA/docs/2018/url-createobjecturl-no-longer-accepts-mediastream-as-argument/).
