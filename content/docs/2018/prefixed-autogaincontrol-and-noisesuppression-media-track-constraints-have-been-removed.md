---
title: "Prefixed `autoGainControl` and `noiseSuppression` media track constraints have been removed"
date: "2018-10-10T11:36:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496714"
      title: "Bug 1496714 - Consider enabling AGC by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1497390"
      title: "Bug 1497390 - Remove support for legacy mozAutoGainControl and mozNoiseSuppression constraints."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Zg6KTgGPp1I/discussion"
      title: "Intent to unship: mozAutoGainControl & mozNoiseSuppression constraints (and AGC=on by default)"
---
The support for the `mozAutoGainControl` and `mozNoiseSuppression` properties on the [`MediaTrackConstraints`](https://developer.mozilla.org/docs/Web/API/MediaTrackConstraints) dictionary, [deprecated since Firefox 55](https://www.fxsitecompat.dev/en-CA/docs/2017/autogaincontrol-and-noisesuppression-media-track-constraints-have-been-unprefixed/), has been removed with Firefox 64. Use the standard, unprefixed [`autoGainControl`](https://developer.mozilla.org/docs/Web/API/MediaTrackConstraints/autoGainControl) and [`noiseSuppression`](https://developer.mozilla.org/docs/Web/API/MediaTrackConstraints/noiseSuppression) properties instead.

Also in Firefox 64, `autoGainControl` will be enabled by default. If you'd like to turn it off, you have to explicitly set the value `false` from now on.
