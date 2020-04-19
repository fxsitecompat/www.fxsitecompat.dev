---
title: "`canPlayType(\'video/webm\')` now returns `\'maybe\'`"
date: "2013-12-09T02:32:17-05:00"
categories: ["audio-video"]
tags: []
versions: ["28", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=884275"
      title: "Bug 884275 – canPlayType(\'video/webm\') should report \'maybe\' instead of \'probably\'"
---
The `canPlayType` method of the [`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) interface has been updated to comply with the spec. `canPlayType('video/webm')` and `canPlayType('audio/webm')` now return `'maybe'` instead of `'probably'`, because media can be encoded with a codec that Firefox doesn't support. If a codec is specified in the `type` argument, the method returns `'probably'` or `''` (empty string) depending on the codec. For example, `canPlayType('video/webm; codecs=vp8')` returns `'probably'`.
