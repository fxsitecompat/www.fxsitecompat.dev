---
title: "`mozAudioContext` has been unprefixed"
date: "2013-02-06T08:44:10-05:00"
categories: ["audio-video"]
tags: []
versions: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=833631"
      title: "Bug 833631 – Unprefix mozAudioContext"
---
The [`mozAudioContext`](https://developer.mozilla.org/docs/Web/API/AudioContext) implementation has been unprefixed. It's still [disabled by default](https://bugzilla.mozilla.org/show_bug.cgi?id=788310), though. To try out this feature, change the value of the `media.webaudio.enabled` pref to `true`.
