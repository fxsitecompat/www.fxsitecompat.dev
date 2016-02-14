---
title: "Firefox 41 以降で MP3 ストリーミング再生に問題が生じます"
date: "2016-01-02T13:37:00-05:00"
categories: ["audio-video"]
tags: []
versions: ["41"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1222866": "Bug 1222866 - Audio pause and distortion in MP3 stream due to rounding error since Firefox 41"
---
MP3 音声のストリーム再生が、停止したり、音の歪みやノイズが生じたりするというリグレッションが Firefox 41 で発生しました。この問題は、再生時間の丸め誤差によるもので、Firefox 43 で修正されました。
