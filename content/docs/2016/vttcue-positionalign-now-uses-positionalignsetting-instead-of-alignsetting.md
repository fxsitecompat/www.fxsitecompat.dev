---
title: "`VTTCue.positionAlign` now uses `PositionAlignSetting` instead of `AlignSetting`"
date: "2016-06-10T09:07:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1276129"
      title: "Bug 1276129 - [webvtt] Use PositionAlignSetting type for VTTCue's positionAlign"
---
Previously, Firefox was incorrectly using an `AlignSetting` for the `VTTCue.prototype.positionAlign` property so that the value could be `start`, `center`, `end`, `left` or `right`. Firefox 49 follows the latest [WebVTT spec](https://w3c.github.io/webvtt/#api) to take and return a `PositionAlignSetting` which is `line-left`, `center`, `line-right` or `auto`.
