---
title: "`navigator.requestMediaKeySystemAccess()` will soon require `MediaKeySystemCapabilities` as configurations"
date: "2017-06-07T09:20:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1368583"
      title: "Bug 1368583 - Add deprecation warning for MediaKeySystemConfigurations without MediaKeySystemCapabilities, or with MediaKeySystemCapabilities with no codecs specified"
---
In order to adhere the Encrypted Media Extensions (EME) spec, the [`navigator.requestMediaKeySystemAccess`](https://developer.mozilla.org/docs/Web/API/Navigator/requestMediaKeySystemAccess) method will soon require developers to supply at least one [`MediaKeySystemConfiguration`](https://developer.mozilla.org/docs/Web/API/MediaKeySystemConfiguration) object containing either [`audioCapabilities`](https://developer.mozilla.org/docs/Web/API/MediaKeySystemConfiguration/audioCapabilities) or [`videoCapabilities`](https://developer.mozilla.org/docs/Web/API/MediaKeySystemConfiguration/videoCapabilities), which must include `contentType` with `codecs` specified. Invalid requests raise a warning in the Web Console on Firefox 55, and will be rejected in the near future.
