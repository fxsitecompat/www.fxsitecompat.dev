---
title: "`VTTCue.positionAlign` が `AlignSetting` の代わりに `PositionAlignSetting` を用いるようになりました"
date: "2016-06-10T09:07:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1276129"
      title: "Bug 1276129 - [webvtt] Use PositionAlignSetting type for VTTCue's positionAlign"
---
これまで Firefox は `VTTCue.prototype.positionAlign` プロパティに誤って `AlignSetting` を用いており、その値は `start`、`center`、`end`、`left`、`right` のいずれかになり得ました。Firefox 49 は最新の [WebVTT 仕様](https://w3c.github.io/webvtt/#api) に従い、`PositionAlignSetting` つまり `line-left`、`center`、`line-right` あるいは `auto` を取り、また返すようになります。
