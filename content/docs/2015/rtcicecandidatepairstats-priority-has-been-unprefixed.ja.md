---
title: "`RTCIceCandidatePairStats.priority` の接頭辞が外れました"
date: "2015-08-05T00:48:18-04:00"
categories: ["audio-video"]
tags: []
releases: ["42", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1184426"
      title: "Bug 1184426 - Unprefix RTCIceCandidatePairStats.priority (formerly mozPriority)"
---
`RTCIceCandidatePairStats.mozPriority` プロパティの接頭辞が外れ、`priority` となりました。
