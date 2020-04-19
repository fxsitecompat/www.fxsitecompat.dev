---
title: "Web Audio API からドップラー効果対応が削除されました"
date: "2018-09-06T16:31:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1148354"
      title: "Bug 1148354 - Remove the doppler effect from the PannerNode"
---
Web Audio API のドップラー効果対応は、その仕様と Firefox 40 以降廃止で予定となっていましたが、Firefox 63 で削除されました。バグのため、この機能は Firefox では常に一部動作していない状態でした。この削除には `AudioListener` インターフェイス上の [`dopplerFactor`](https://developer.mozilla.org/docs/Web/API/AudioListener/dopplerFactor)、[`speedOfSound`](https://developer.mozilla.org/docs/Web/API/AudioListener/speedOfSound) 両プロパティ、ならびに `AudioListener`、`PannerNode` 両インターフェイス上の [`setVelocity`](https://developer.mozilla.org/docs/Web/API/PannerNode/setVelocity) メソッドが含まれます。
