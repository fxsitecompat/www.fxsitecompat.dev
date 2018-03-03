---
title: "様々な端末センサー API が廃止予定となりました"
date: "2018-03-02T20:53:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1359076"
      title: "Bug 1359076 - Disable devicelight, deviceproximity and userproximity events"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DcSi_wLG4fc/discussion"
      title: "Intent to remove Ambient Light and Proximity sensor APIs"
---
ユーザーのプライバシーを守るため、Firefox は端末の [向き、動き](https://developer.mozilla.org/ja/docs/Web/API/Detecting_device_orientation)、[近接](https://developer.mozilla.org/ja/docs/Web/API/Proximity_Events)、[環境光](https://developer.mozilla.org/ja/docs/Web/API/Ambient_Light_Events) イベントへの対応を廃止予定としました。これらのセンサー API はウェブアプリをネイティブモバイルアプリへより近づけるものですが、その強力な性質上、ブラウザーのフィンガープリンティングや [同一オリジンポリシー](https://developer.mozilla.org/ja/docs/Web/Security/Same-origin_policy) 違反に悪用される恐れがあります。

`devicelight`、`deviceproximity`、`userproximity` の各イベントは、Firefox 60 以降 Nightly と早期 Beta/DevEdition チャンネルでは初期設定で無効化されており、Firefox 62 以降すべてのチャンネルで無効化されます。現時点ではブラウザー対応が限られることから、互換性リスクは最小限のはずです。無効化された場合、単にイベントが発生しなくなります。

一方、`deviceorientation`、`devicemotion` 両イベントは、WebVR を含めて妥当なユースケースがあることからまだ使用可能です。開発者はその方向性についてより詳しく議論する予定です。
