---
title: "`RTCRtpTransceiver.mid` が接頭辞なしのメディア ID を返すようになりました"
date: "2018-08-31T04:03:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["63", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1476600"
      title: "Bug 1476600 - Mid from stopped transceiver is reused"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1482250"
      title: "Bug 1482250 - Mid \"0\" is a foot-gun (caused some JS library breakage)."
---
従来、`RTCRtpTransceiver` インターフェイス上の [`mid`](https://developer.mozilla.org/docs/Web/API/RTCRtpTransceiver/mid) プロパティは、`"sdparta_0"` や `"sdparta_1"` など `sdparta_` という接頭辞の付いたメディア ID を返していました。仕様が短い値を推奨していることや Google Chrome が現時点で接頭辞を使用していないことから、Firefox 63 で接頭辞が外され、単に `"0"` や `"1"` といった文字列型の数字を返すようになりました。

一部の WebRTC ライブラリなど特定のスクリプトはこの変更による影響を受けているようです。これは、プロパティが返す可能性のある `null` に加えて、`"0"` が JavaScript では偽とみなされる値であるためです。値を確認する際には厳密な比較を行ってください。

```js
"0" == false // true
"0" === false // false
Number("0") // 0
Number(null) // 0
parseInt("0") // 0
parseInt(null) // NaN
```
