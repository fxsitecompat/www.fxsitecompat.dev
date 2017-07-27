---
title: "`autoGainControl` and `noiseSuppression` media track constraints have been unprefixed"
date: "2017-05-21T23:41:00-05:00"
categories: ["audio-video"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1366415"
      title: "Bug 1366415 - Unprefix autoGainControl and noiseSuppression constraints"
---
The `autoGainControl` and `noiseSuppression` properties on the [`MediaTrackConstraints`](https://developer.mozilla.org/en-US/docs/Web/API/MediaTrackConstraints) dictionary are now available unprefixed. These `moz`-prefixed versions will be removed in the near future.
