---
title: "`RTCDataChannel.stream` が削除されました"
date: "2016-06-24T14:06:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=878945"
      title: "Bug 878945 - Update DataChannel WebIDL to match spec changes (renaming dictionary values)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1281150"
      title: "Bug 1281150 - Remove obsolete RTCDataChannel.stream property"
---
仕様変更のため Firefox 22 以降廃止予定となっていた [`RTCDataChannel.prototype.stream`](https://developer.mozilla.org/docs/Web/API/RTCDataChannel/stream) プロパティは Firefox 50 以降使用できません。標準化された [`id`](https://developer.mozilla.org/docs/Web/API/RTCDataChannel/id) プロパティを代用してください。
