---
title: "`getUserMedia()` and `enumerateDevices()` can no longer be used on insecure sites"
date: "2019-05-28T02:56:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
versions: ["68"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335740"
      title: "Bug 1335740 - Disable getUserMedia on non-secure origins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528031"
      title: "Bug 1528031 - Make navigator.mediaDevices SecureContext (removing it in http)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vmO0NRM46l8/discussion"
      title: "Intent to deprecate: insecure getUserMedia & enumerateDevices requests"
---
Starting with Firefox 68, the `getUserMedia` and `enumerateDevices` methods on the [`MediaDevices`](https://developer.mozilla.org/docs/Web/API/MediaDevices) interface only work on websites served via HTTPS. When these methods are called on insecure sites, a `NotAllowedError` exception will be thrown. [Google Chrome](https://www.chromestatus.com/feature/5703419427815424) has already made the change in version 47, and less than 3% of sites are affected according to Mozilla's Telemetry data.

In the near future, the `navigator.mediaDevices` object and the `navigator.mozGetUserMedia` method will also require secure origins as per the current Media Capture and Streams spec. Make sure to always serve your site via HTTPS.
