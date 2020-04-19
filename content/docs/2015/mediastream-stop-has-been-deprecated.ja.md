---
title: "`MediaStream.stop()` が廃止予定となりました"
date: "2015-10-01T16:06:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1103188"
      title: "Bug 1103188 - Implement MediaStream.addTrack()/removeTrack()"
---
[`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) インターフェイス上の `stop` は、WebRTC 仕様から削除され、Firefox 44 で廃止予定となりました。ストリーミングを停止するには、以下のコードサンプルが示すように [`MediaStreamTrack.stop`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack/stop) メソッドを代わりに使用してください。

```js
navigator.mediaDevices.getUserMedia({
  audio: false,
  video: true
}).then(stream => {
  // stream.stop(); // 廃止予定
  stream.getVideoTracks()[0].stop(); // 推奨
});
```

[開発者によれば](https://bugzilla.mozilla.org/show_bug.cgi?id=1103188#c106)、最新の仕様に準拠するため WebRTC 実装にあといくつかの変更が予定されています。後方互換性に影響する変更があればこのサイトにドキュメントを追加します。
