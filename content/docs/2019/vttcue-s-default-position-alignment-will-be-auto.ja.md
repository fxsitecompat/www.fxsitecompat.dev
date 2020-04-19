---
title: "`VTTCue` の既定配置が `auto` となります"
date: "2019-05-13T03:03:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528420"
      title: "Bug 1528420 - [webvtt] Cue's positionAlign should be `auto` by default"
---
Firefox 67 以降、`VTTCue` オブジェクト上の `positionAlign` プロパティ既定値が、現行の [WebVTT 仕様](https://w3c.github.io/webvtt/#webvtt-cue-position-alignment) に従って、`center` ではなく `auto` となります。必要な場合は値を変更してください。
