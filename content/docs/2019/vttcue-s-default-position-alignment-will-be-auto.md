---
title: "`VTTCue`'s default position alignment will be `auto`"
date: "2019-05-13T03:03:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528420"
      title: "Bug 1528420 - [webvtt] Cue's positionAlign should be `auto` by default"
---
On Firefox 67 and later, the `positionAlign` property on a `VTTCue` object will be defaulted to `auto` instead of `center`, according to the current [WebVTT spec](https://w3c.github.io/webvtt/#webvtt-cue-position-alignment). Change the value if needed.
