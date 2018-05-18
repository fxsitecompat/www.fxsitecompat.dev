---
title: "Ambient light and proximity sensor APIs have been disabled"
date: "2018-05-18T00:15:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1462308"
      title: "Bug 1462308 - Disable devicelight, deviceproximity and userproximity events from stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DcSi_wLG4fc/discussion"
      title: "Intent to remove Ambient Light and Proximity sensor APIs"
---
The support for the [Ambient Light Sensor](https://developer.mozilla.org/docs/Web/API/Ambient_Light_Events) and [Proximity Sensor](https://developer.mozilla.org/docs/Web/API/Proximity_Events) APIs, the [`devicelight`](https://developer.mozilla.org/docs/Web/Events/devicelight), [`deviceproximity`](https://developer.mozilla.org/docs/Web/Events/deviceproximity) and [`userproximity`](https://developer.mozilla.org/docs/Web/Events/userproximity) events in particular, have been disabled by default with Firefox 62 due to concerns over user privacy and [same-origin policy](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) violations.

Those APIs have already been disabled in the Nightly and early Beta/DevEdition channels since the [version 60](https://www.fxsitecompat.com/en-CA/docs/2018/various-device-sensor-apis-are-now-deprecated/), and no issues have been reported so far. Given that the browser support is very limited at this time, the compatibility impact should be minimal.
