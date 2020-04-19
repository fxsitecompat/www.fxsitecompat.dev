---
title: "MP3 streaming is awkward on Firefox 41 and later"
date: "2016-01-02T13:37:00-05:00"
categories: ["audio-video"]
tags: []
releases: ["41"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222866"
      title: "Bug 1222866 - Audio pause and distortion in MP3 stream due to rounding error since Firefox 41"
---
Firefox 41 has introduced a regression where MP3 audio stream playback may pause, distort or make noises. The issue, caused by the duration time rounding error, has been fixed with Firefox 43.
