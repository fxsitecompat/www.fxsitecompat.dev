---
title: "`getUserMedia()` が安全でないサイトでは使用できなくなりました"
date: "2019-05-28T02:56:00-04:00"
categories: ["audio-video", "privacy-security"]
tags: []
versions: ["68", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335740"
      title: "Bug 1335740 - Disable getUserMedia on non-secure origins"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vmO0NRM46l8/discussion"
      title: "Intent to deprecate: insecure getUserMedia & enumerateDevices requests"
    - url: "https://blog.mozilla.org/webrtc/camera-microphone-require-https-in-firefox-68/"
      title: "Advancing WebRTC: Camera & microphone require https in Firefox 68."
aliases:
    - "/ja/docs/2019/getusermedia-and-enumeratedevices-can-no-longer-be-used-on-insecure-sites/"
---
Firefox 68 以降、[`MediaDevices`](https://developer.mozilla.org/docs/Web/API/MediaDevices) インターフェイス上の `getUserMedia` メソッドは HTTPS で配信されたウェブサイトでのみ動作します。これらのメソッドが安全でないサイト上で呼ばれた場合、`NotAllowedError` 例外が投げられます。[Google Chrome](https://www.chromestatus.com/feature/5703419427815424) は既にバージョン 47 でこの変更を行っており、Mozilla の Telemetry データによれば影響を受けるサイトは 3% 未満です。

近い将来、`navigator.mediaDevices` オブジェクトと `navigator.mozGetUserMedia` メソッドも、現行の Media Capture and Streams 仕様に従って安全なオリジンを必要とします。あなたのサイトを常に HTTPS で配信するようにしてください。

**更新**: この記事の初版は `enumerateDevices` メソッドにも言及していましたが、これは Firefox 68 ではまだ使用可能です。フィードバックを受けてタイトルと説明を訂正し、WebRTC ブログへのリンクを追加しました。

**更新 2**: [Firefox 69](https://www.fxsitecompat.dev/ja/docs/2019/navigator-mediadevices-and-navigator-mozgetusermedia-can-no-longer-be-used-on-insecure-sites/) 以降、`navigator.mediaDevices` オブジェクトと `navigator.mozGetUserMedia` メソッドは安全でないサイトでは使用できなくなりました。
