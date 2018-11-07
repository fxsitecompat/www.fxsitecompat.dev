---
title: "`MediaStream.currentTime` が削除されました"
date: "2018-11-06T12:06:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1502927"
      title: "Bug 1502927 - Remove MediaStream.currentTime"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/QW7_dfNSWLw/discussion"
      title: "Intent to unship: MediaStream.currentTime"
---
Firefox 65 で非標準の `currentTime` プロパティが `MediaStream` インターフェイスから削除されました。これは一度も仕様で標準化されたことはなく、他のブラウザーに実装されることもなかったため、削除のリスクは非常に低いはずです。
