---
title: "接頭辞付き `autoGainControl`、`noiseSuppression` メディアトラック制約が廃止されました"
date: "2018-10-10T11:36:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496714"
      title: "Bug 1496714 - Consider enabling AGC by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1497390"
      title: "Bug 1497390 - Remove support for legacy mozAutoGainControl and mozNoiseSuppression constraints."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Zg6KTgGPp1I/discussion"
      title: "Intent to unship: mozAutoGainControl & mozNoiseSuppression constraints (and AGC=on by default)"
---
[Firefox 55 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2017/autogaincontrol-and-noisesuppression-media-track-constraints-have-been-unprefixed/) [`MediaTrackConstraints`](https://developer.mozilla.org/docs/Web/API/MediaTrackConstraints) ディクショナリー上の `mozAutoGainControl`、`mozNoiseSuppression` 両プロパティへの対応が Firefox 64 で削除されました。標準の接頭辞なしプロパティ [`autoGainControl`](https://developer.mozilla.org/docs/Web/API/MediaTrackConstraints/autoGainControl)、[`noiseSuppression`](https://developer.mozilla.org/docs/Web/API/MediaTrackConstraints/noiseSuppression) を代わりに使用してください。

Firefox 64 ではまた、`autoGainControl` が初期設定で有効となります。無効にしたい場合、今後は明示的に値を `false` に設定する必要があります。
