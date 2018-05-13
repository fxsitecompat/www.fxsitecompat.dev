---
title: "Audio Data API が無効化されました"
date: "2013-12-09T02:32:17-05:00"
categories: ["audio-video"]
tags: []
versions: ["28"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=927245"
      title: "Bug 927245 – Remove deprecated Audio Data API implementation"
---
[Firefox 22 以降非推奨となっていた](https://www.fxsitecompat.com/ja/docs/2013/audio-data-api-has-been-deprecated/) 実験的で非標準の [Audio Data API](https://developer.mozilla.org/docs/Introducing_the_Audio_API_Extension) が、設定 `media.audio_data.enabled` で無効化されました。この API は [Firefox 31 で削除されます](https://www.fxsitecompat.com/ja/docs/2014/audio-data-api-has-been-removed/)。標準の [Web Audio API](https://developer.mozilla.org/docs/Web_Audio_API) を代わりに使ってください。
