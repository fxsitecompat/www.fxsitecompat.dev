---
title: "`navigator.mediaDevices` and `navigator.mozGetUserMedia()` can no longer be used on insecure sites"
date: "2019-07-06T20:43:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
versions: ["69"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528031"
      title: "Bug 1528031 - Make navigator.mediaDevices SecureContext (removing it in http)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vmO0NRM46l8/discussion"
      title: "Intent to deprecate: insecure getUserMedia & enumerateDevices requests"
    - url: "https://blog.mozilla.org/webrtc/camera-microphone-require-https-in-firefox-68/"
      title: "Advancing WebRTC: Camera & microphone require https in Firefox 68."
---
Starting with Firefox 69, the `navigator.mediaDevices` object and the non-standard `navigator.mozGetUserMedia` method are only available to websites served via HTTPS. Calling the `getUserMedia`, `enumerateDevices` or any other method on the `navigator.mediaDevices` object on an insecure site will throw a `TypeError` exception because the object doesn't exist. Google Chrome has already made the same change in version 74.

Note that the `getUserMedia` method has already been available only to secure sites in [Firefox 68](https://www.fxsitecompat.dev/en-CA/docs/2019/getusermedia-can-no-longer-be-used-on-insecure-sites/). Meanwhile, these methods will continue to be available to `http://localhost` which is considered as a secure origin, so web developers can test camera and microphone features in a local environment. The production site, however, has to be served via HTTPS at any time.
