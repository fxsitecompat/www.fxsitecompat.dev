---
title: "`navigator.requestMediaKeySystemAccess()` は近いうちに `MediaKeySystemCapabilities` 設定が必須となります"
date: "2017-06-07T09:20:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1368583"
      title: "Bug 1368583 - Add deprecation warning for MediaKeySystemConfigurations without MediaKeySystemCapabilities, or with MediaKeySystemCapabilities with no codecs specified"
---
Encrypted Media Extensions (EME) 仕様に準拠するため、[`navigator.requestMediaKeySystemAccess`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/requestMediaKeySystemAccess) メソッドはまもなく、少なくともひとつの [`MediaKeySystemConfiguration`](https://developer.mozilla.org/ja/docs/Web/API/MediaKeySystemConfiguration) オブジェクトを与えるよう開発者に求めることとなります。これは [`audioCapabilities`](https://developer.mozilla.org/ja/docs/Web/API/MediaKeySystemConfiguration/audioCapabilities) もしくは [`videoCapabilities`](https://developer.mozilla.org/ja/docs/Web/API/MediaKeySystemConfiguration/videoCapabilities) であり、`codecs` を指定した `contentType` を含めなければなりません。不正なリクエストは Firefox 55 上のウェブコンソールに警告を表示させ、近い将来拒絶されるようになります。
