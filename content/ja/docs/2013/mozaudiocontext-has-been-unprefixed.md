---
title: "`mozAudioContext` の接頭辞が外れました"
date: "2013-02-06T08:44:10-05:00"
categories: ["audio-video"]
tags: []
versions: "21"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=833631": "Bug 833631 – Unprefix mozAudioContext"
---
[`mozAudioContext`](https://developer.mozilla.org/ja/docs/Web/API/AudioContext) の実装から接頭辞が外れました。ただし、まだ [初期設定では無効](https://bugzilla.mozilla.org/show_bug.cgi?id=788310) となっています。この機能を試すには、`media.webaudio.enabled` の設定値を `true` に変更してください。
