---
title: "Firefox for Android UA string now has the Android version"
date: "2015-06-13T15:20:46-04:00"
categories: ["networking"]
tags: []
releases: ["41", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1169772"
      title: "Bug 1169772 - Add Android version number to Fennec UA String"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1174784"
      title: "Bug 1174784 - Youtube video playback broken with Android version in UA string"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1193354"
      title: "Bug 1193354 - play.google.com - No image appearing on Firefox for Android"
---
The user-agent (UA) string of [Firefox for Android](https://developer.mozilla.org/Firefox_for_Android) now contains the device's Android version as part of the platform token. See the [Gecko UA string reference](https://developer.mozilla.org/docs/Web/HTTP/Gecko_user_agent_string_reference#Android_%28version_41_and_above%29) for details. If you have mobile UA detection code, make sure it still works. So far, video playback on *YouTube* and image display on *Google Play* are known to be broken.
