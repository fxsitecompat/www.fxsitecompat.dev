---
title: "Various device sensor APIs are now deprecated"
date: "2018-03-02T20:53:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1359076"
      title: "Bug 1359076 - Disable devicelight, deviceproximity and userproximity events"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DcSi_wLG4fc/discussion"
      title: "Intent to remove Ambient Light and Proximity sensor APIs"
---
In an effort to protect user privacy, Firefox has deprecated the support for the device [orientation, motion](https://developer.mozilla.org/docs/Web/API/Detecting_device_orientation), [proximity](https://developer.mozilla.org/docs/Web/API/Proximity_Events) and [ambient light](https://developer.mozilla.org/docs/Web/API/Ambient_Light_Events) events. Those sensor APIs make web apps more like native mobile apps, but given the powerful nature, they can be misused for browser fingerprinting or [same-origin policy](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) violations.

The `devicelight`, `deviceproximity` and `userproximity` events are disabled by default in the Nightly and early Beta/DevEdition channels, starting with Firefox 60. The support will be disabled in the all channels with Firefox 62. The compatibility risk should be minimal since the browser support is limited at this time. Once disabled, the events just won't be fired.

The `deviceorientation` and `devicemotion` events, on the other hand, are still available given legitimate use cases including WebVR. Developers will be discussing more about the direction.

**Update**: The ambient light and proximity sensor APIs have been disabled with [Firefox 62](https://www.fxsitecompat.com/en-CA/docs/2018/ambient-light-and-proximity-sensor-apis-have-been-disabled/) as planned.
