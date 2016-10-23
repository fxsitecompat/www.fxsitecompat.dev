---
title: "`onpointer*` は初期設定で隠しプロパティとなります"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom"]
tags: []
versions: ["34"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1017086"
      title: "Bug 1017086 – Don\'t expose onpointer* on global when dom.w3c_pointer_events.enabled is false"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1015600"
      title: "Bug 1015600 – Mobile Google Play menu does not work on Firefox for Android (pointerdown and pointerup events do not fire even though feature detection indicates support)"
---
これまで、ポイントイベントハンドラー (`onpointerup`、`onpointerover`、`onpointerout`、`onpointermove`、`onpointerleave`、`onpointerenter`、`onpointerdown`、`onpointercancel`) が、[Pointer Events API](http://www.w3.org/TR/pointerevents/) 無効時にも誤ってグローバルオブジェクトへ露呈されていました。この API はまだ初期設定で有効化されていません。*Google Play* がこのバグの影響を受けており、`onpointerup` を使用した機能判別が動作する一方でイベント自体はまったく実行されないという状況が確認されていました。これらのプロパティは API 無効時には露呈されなくなります。
