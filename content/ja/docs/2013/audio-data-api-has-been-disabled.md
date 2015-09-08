---
title: "Audio Data API が無効化されました"
date: "2013-12-09T02:32:17-05:00"
categories: ["audio-video"]
tags: []
versions: "28"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=927245": "Bug 927245 – Remove deprecated Audio Data API implementation"
---
[Firefox 22](http://www.fxsitecompat.com/ja/versions/22/) 以降非推奨となっていた実験的で非標準の [Audio Data API](https://developer.mozilla.org/ja/docs/Introducing_the_Audio_API_Extension) が、設定 `media.audio_data.enabled` で無効化されました。この API は [Firefox 31](http://www.fxsitecompat.com/ja/versions/31/) で削除されます。標準の [Web Audio API](https://developer.mozilla.org/ja/docs/Web_Audio_API) を代わりに使ってください。
