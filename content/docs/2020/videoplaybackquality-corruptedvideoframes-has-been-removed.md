---
title: "`VideoPlaybackQuality.corruptedVideoFrames` has been removed"
date: "2020-01-06T22:46:00-05:00"
categories: ["audio-video"]
tags: []
releases: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1602163"
      title: "Bug 1602163 - VideoPlaybackQuality corruptedFrames deprecated"
---
Firefox 73 has removed the read-only [`corruptedVideoFrames`](https://developer.mozilla.org/docs/Web/API/VideoPlaybackQuality/corruptedVideoFrames) property from the `VideoPlaybackQuality` interface, because it was dropped from the spec. Major corruptions may lead to a decode error, while minor ones may just produce artifacts in the output, so the property wasn't useful.
