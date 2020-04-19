---
title: "Some `KeyboardEvent.key` values have been renamed"
date: "2016-06-10T09:54:00-04:00"
categories: ["dom"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1272578"
      title: "Bug 1272578 - [UI Events-key] Rename VolumeDown, VolumeUp and VolumeMute to AudioVolumeDown, AudioVolumeUp and AudioVolumeMute"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1272592"
      title: "Bug 1272592 - [UI Events-key] Drop \"MediaSelect\" key value and use \"LaunchMediaPlayer\" instead"
---
Several key values returned by the [`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/key) property have been updated for the latest DOM Level 3 Events spec. `VolumeDown`, `VolumeUp` and `VolumeMute` are now `AudioVolumeDown`, `AudioVolumeUp` and `AudioVolumeMute` respectively. `MediaSelect` has been removed in favour of `LaunchMediaPlayer`.
