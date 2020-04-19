---
title: "WebRTC video may stop in low-bandwidth conditions"
date: "2017-10-24T18:21:00-04:00"
categories: ["audio-video"]
tags: []
releases: ["56"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403714"
      title: "Bug 1403714 - Firefox stops sending video in low-bandwidth conditions and doesn't recover"
---
Firefox 56 has introduced a regression where sending video may stop in a WebRTC call, especially with multiple participants and in a limited bandwidth. The situation won't improve once Firefox halts sending video packets, while the audio continues working. This bug has been fixed with Firefox 56.0.2.
