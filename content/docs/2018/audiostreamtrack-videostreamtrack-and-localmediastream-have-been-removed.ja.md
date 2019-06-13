---
title: "`AudioStreamTrack`、`VideoStreamTrack`、`LocalMediaStream` が廃止されました"
date: "2018-10-23T02:50:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1258143"
      title: "Bug 1258143 - Remove LocalMediaStream (and its Stop()) from js"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1377146"
      title: "Bug 1377146 - Remove AudioStreamTrack and VideoStreamTrack"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dPyxsKABnKY/discussion"
      title: "Intent to unship: AudioStreamTrack and VideoStreamTrack"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/mA200p2N-Hk/discussion"
      title: "Intent to unship: LocalMediaStream"
---
[`MediaStreamTrack`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack) のサブクラスだった `AudioStreamTrack`、`VideoStreamTrack` 両インターフェイスが Firefox 64 で削除されました。Firefox は 2014 年に Media Capture and Streams 仕様から削除されたこれらの古いインターフェイスに対応していた唯一のブラウザーでした。必要であれば、`MediaStreamTrack` オブジェクトの種類は [`kind`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack/kind) プロパティを用いて判別可能です。

[`LocalMediaStream`](https://developer.mozilla.org/docs/Web/API/LocalMediaStream) インターフェイスも同時に削除されました。[`getUserMedia`](https://developer.mozilla.org/docs/Web/API/MediaDevices/getUserMedia) メソッドは今後、Firefox にしか実装されていなかった `LocalMediaStream` の代わりに [`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) オブジェクトを返します。[Firefox 44 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2015/mediastream-stop-has-been-deprecated/) `stop` メソッドは、以下で示すように、`MediaStreamTrack` インターフェイス上の [`stop`](https://developer.mozilla.org/docs/Web/API/MediaStreamTrack/stop) メソッドと置き換えられます。

```js
navigator.mediaDevices.getUserMedia({
  audio: false,
  video: true
}).then(stream => {
  // stream.stop() の代わりに以下のようにしてください:
  stream.getVideoTracks()[0].stop();
});
```
