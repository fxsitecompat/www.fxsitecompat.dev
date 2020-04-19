---
title: "Geolocation, fullscreen, camera, mic, screen capture requests from cross-origin `<iframe>` are now disabled by default"
date: "2020-01-05T20:13:00-05:00"
categories: ["audio-video", "dom", "privacy-security"]
tags: []
releases: ["74"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1483631"
      title: "Bug 1483631 - Restrict nested permission requests (camera/microphone/geolocation/screensharing) with Feature Policy"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503694"
      title: "Bug 1503694 - FeaturePolicy: Hangouts cannot access microphone from Gmail"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1563758"
      title: "Bug 1563758 - Fullscreen button is not functional on AOL websites"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1579373"
      title: "Bug 1579373 - Disabling geolocation permissions by default in cross-origin iframes"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583142"
      title: "Bug 1583142 - Considering removing third-party \"persistent-storage\" prompting support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1595720"
      title: "Bug 1595720 - Set Feature Policy default allow list for fullscreen to eself, disable third party by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1600883"
      title: "Bug 1600883 - Enable Feature Policy allow attribute and permission delegation by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610572"
      title: "Bug 1610572 - Disable Feature Policy for FF73"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1617219"
      title: "Bug 1617219 - Enable Feature Policy & Permission Delegation for Release 74"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/BdFOMAuCGW8/discussion"
      title: "Intent to prototype: Delegate and restrict permission in third party context"
aliases:
    - "/en-CA/docs/2012/geolocation-fullscreen-camera-mic-screen-capture-requests-from-cross-origin-iframe-are-now-disabled-by-default/"
---
Firefox 74 has added the support for [Feature Policy](https://developer.mozilla.org/docs/Web/HTTP/Feature_Policy) that allows web developers to control the behaviour of various web platform features and APIs. The new `allow` attribute on the `<iframe>` element can be used to control features within the `<iframe>`, where certain features are now disabled for third parties by default in an effort to avoid confusion for users.

These features can no longer be used in cross-origin `<iframe>`s unless the feature is explicitly enabled with the `allow` attribute:

* Geolocation API: [`geolocation`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/geolocation) directive
* Fullscreen API: [`fullscreen`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/fullscreen) directive
* Camera and mic access: [`camera`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/camera) and [`microphone`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/microphone) directives
* Screen Capture API: [`display-capture`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Feature-Policy/display-capture) directive

So, for example, if you'd like to allow a third-party `<iframe>` to use the Geolocation API, you have to write something like this, otherwise their permission request will be silently blocked:

```html
<iframe src="https://maps.example.com/" allow="geolocation"></iframe>
```

These features can no longer be used in cross-origin `<iframe>`s even if you use the `allow` attribute:

* Persistent storage via `navigator.storage.persist()`
* Notifications API (since [Firefox 70](https://www.fxsitecompat.dev/en-CA/docs/2019/notification-permission-requests-from-cross-origin-iframe-are-now-disallowed/))
* Vibration API (since [Firefox 72](https://www.fxsitecompat.dev/en-CA/docs/2019/vibration-api-can-no-longer-be-used-from-cross-origin-iframe/))

**Update**: The change has been postponed from Firefox 73 to 74.

**Update 2**: *Google Hangouts* is affected by this change, where mic access from *Gmail* doesn’t work. Also, video players’ fullscreen button is not working on *AOL*-owned web properties including *HuffPost*, *Engadget* and *TechCrunch*.
