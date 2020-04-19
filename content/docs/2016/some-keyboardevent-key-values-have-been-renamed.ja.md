---
title: "`KeyboardEvent.key` の値が一部変更されました"
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
[`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/key) プロパティによって返されるいくつかのキー値が、最新の DOM Level 3 Events 仕様に合わせて更新されました。`VolumeDown`、`VolumeUp`、`VolumeMute` はそれぞれ `AudioVolumeDown`、`AudioVolumeUp`、`AudioVolumeMute` となりました。`MediaSelect` は `LaunchMediaPlayer` に取って代わられる形で削除されました。
