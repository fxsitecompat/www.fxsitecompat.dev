---
title: "環境光・近接センサー API が無効化されました"
date: "2018-05-18T00:15:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1462308"
      title: "Bug 1462308 - Disable devicelight, deviceproximity and userproximity events from stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DcSi_wLG4fc/discussion"
      title: "Intent to remove Ambient Light and Proximity sensor APIs"
---
[環境光センサー](https://developer.mozilla.org/docs/Web/API/Ambient_Light_Events) と [近接センサー](https://developer.mozilla.org/docs/Web/API/Proximity_Events) API、具体的には [`devicelight`](https://developer.mozilla.org/docs/Web/Events/devicelight)、[`deviceproximity`](https://developer.mozilla.org/docs/Web/Events/deviceproximity)、[`userproximity`](https://developer.mozilla.org/docs/Web/Events/userproximity) イベントへの対応が、ユーザーのプライバシーと [同一オリジンポリシー](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) 違反を巡る懸念から、Firefox 62 以降初期設定で無効化されました。

これらの API は、[バージョン 60](https://www.fxsitecompat.com/ja/docs/2018/various-device-sensor-apis-are-now-deprecated/) 以降 Nightly と早期 Beta/DevEdition チャンネルでは無効化されており、今のところ特に問題は報告されていません。現時点でブラウザー対応が非常に限られていることから、互換性への影響は軽微なはずです。
