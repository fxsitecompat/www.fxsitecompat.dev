---
title: "`RTCRtpTransceiver.mid` now returns media ID without prefix"
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
Previously, the [`mid`](https://developer.mozilla.org/docs/Web/API/RTCRtpTransceiver/mid) property on the `RTCRtpTransceiver` interface was returning a media ID prefixed with `sdparta_`, such as `"sdparta_0"` or `"sdparta_1"`. Given that the spec recommends shorter values and Google Chrome uses no prefix at this time, Firefox 63 has dropped the prefix to just return a number in string, like `"0"` or `"1"`.

Certain scripts including some WebRTC libraries are apparently broken due to this change, because, in addition to `null` the property may return, `"0"` is a falsy value in JavaScript. Make a strict comparison when checking the values.

```js
"0" == false // true
"0" === false // false
Number("0") // 0
Number(null) // 0
parseInt("0") // 0
parseInt(null) // NaN
```
