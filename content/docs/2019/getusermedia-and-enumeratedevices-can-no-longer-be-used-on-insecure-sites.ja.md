---
title: "`getUserMedia()` と `enumerateDevices()` が安全でないサイトでは使用できなくなりました"
date: "2019-05-28T02:56:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
versions: ["68"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335740"
      title: "Bug 1335740 - Disable getUserMedia on non-secure origins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528031"
      title: "Bug 1528031 - Make navigator.mediaDevices SecureContext (removing it in http)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vmO0NRM46l8/discussion"
      title: "Intent to deprecate: insecure getUserMedia & enumerateDevices requests"
---
Firefox 68 以降、[`MediaDevices`](https://developer.mozilla.org/docs/Web/API/MediaDevices) インターフェイス上の `getUserMedia`、`enumerateDevices` 両メソッドは HTTPS で配信されたウェブサイトでのみ動作します。これらのメソッドが安全でないサイト上で呼ばれた場合、`NotAllowedError` 例外が投げられます。[Google Chrome](https://www.chromestatus.com/feature/5703419427815424) は既にバージョン 47 でこの変更を行っており、Mozilla の Telemetry データによれば影響を受けるサイトは 3% 未満です。

近い将来、`navigator.mediaDevices` オブジェクトと `navigator.mozGetUserMedia` メソッドも、現行の Media Capture and Streams 仕様に従って安全なオリジンを必要とします。あなたのサイトを常に HTTPS で配信するようにしてください。
