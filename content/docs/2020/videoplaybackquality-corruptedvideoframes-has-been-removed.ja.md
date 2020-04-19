---
title: "`VideoPlaybackQuality.corruptedVideoFrames` が廃止されました"
date: "2020-01-06T22:46:00-05:00"
categories: ["audio-video"]
tags: []
releases: ["73"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1602163"
      title: "Bug 1602163 - VideoPlaybackQuality corruptedFrames deprecated"
---
`VideoPlaybackQuality` インターフェイス上の読み取り専用 [`corruptedVideoFrames`](https://developer.mozilla.org/docs/Web/API/VideoPlaybackQuality/corruptedVideoFrames) プロパティが、仕様からの削除に伴い、Firefox 73 で廃止されました。重大なデータ破損はデコードエラーにつながる可能性があり、一方で軽微な破損は単に出力にノイズを生むだけで、このプロパティは役に立っていませんでした。
