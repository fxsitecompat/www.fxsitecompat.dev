---
title: "Doppler effect support has been removed from Web Audio API"
date: "2018-09-06T16:31:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1148354"
      title: "Bug 1148354 - Remove the doppler effect from the PannerNode"
---
The Doppler effect support in the Web Audio API, which had been deprecated in the spec and since Firefox 40, has been removed with Firefox 63. Due to a bug, the feature had always been partially broken in Firefox. This removal includes the [`dopplerFactor`](https://developer.mozilla.org/docs/Web/API/AudioListener/dopplerFactor) and [`speedOfSound`](https://developer.mozilla.org/docs/Web/API/AudioListener/speedOfSound) properties on the `AudioListener` interface as well as the [`setVelocity`](https://developer.mozilla.org/docs/Web/API/PannerNode/setVelocity) method on the `AudioListener` and `PannerNode` interfaces.
