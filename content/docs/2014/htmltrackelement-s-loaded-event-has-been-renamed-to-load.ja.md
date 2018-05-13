---
title: "`HTMLTrackElement` の `loaded` イベントが `load` へ変更されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["audio-video"]
tags: []
versions: ["33"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035505"
      title: "Bug 1035505 – [webvtt] HTMLTrackElement should fire a \'load\' event not a \'loaded\'"
---
[`HTMLTrackElement`](https://developer.mozilla.org/docs/Web/API/HTMLTrackElement) インターフェイスの実装が更新され、最新の仕様に従って `loaded` ではなく `load` イベントを発行するようになりました。
