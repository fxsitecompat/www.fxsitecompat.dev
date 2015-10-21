---
title: "制約的 `RTCOfferOptions` への対応が打ち切られました"
date: "2015-09-09T15:49:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1063808": "Bug 1063808 - createOffer options spec-change to RTCOfferOptions abruptly breaks things in 33"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1064223": "Bug 1064223 - Retire backwards compatible RTCOfferOptions in about 6 weeks"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1197021": "Bug 1197021 - Really retire backwards compatible RTCOfferOptions in 44"
---
廃止予定となっており、Firefox 33 で一度削除されたものの、後方互換性のためすぐに警告付きで元に戻された、制約的 `RTCOfferOptions` への対応が Firefox 43 から削除されました。以下のような古い構文は今後動作しなくなり、Firefox 44 まではエラーがログに残されます。

```js
var options = {
    mandatory: { OfferToReceiveAudio: true },
    optional: [{ OfferToReceiveVideo: true }]
};
```

これが [新しい構文](https://developer.mozilla.org/ja/docs/Web/API/WebRTC_API/WebRTC_basics#options) です。大文字・小文字の違いに注意してください。

```js
var options = {
    offerToReceiveAudio: true,
    offerToReceiveVideo: true
};
```
