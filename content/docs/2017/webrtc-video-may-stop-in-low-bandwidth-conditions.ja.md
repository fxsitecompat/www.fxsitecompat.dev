---
title: "低帯域環境で WebRTC 動画が止まってしまう場合があります"
date: "2017-10-24T18:21:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["56"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403714"
      title: "Bug 1403714 - Firefox stops sending video in low-bandwidth conditions and doesn't recover"
---
WebRTC 通話内で、特に複数の参加者がいて限られた帯域幅で接続している場合に、動画の送信が止まってしまう場合があるというリグレッションが Firefox 56 で発生しました。一度 Firefox が動画パケットの送信を止めてしまうと、音声は流れ続けるものの、状況は改善しません。このバグは Firefox 56.0.2 で修正されました。
