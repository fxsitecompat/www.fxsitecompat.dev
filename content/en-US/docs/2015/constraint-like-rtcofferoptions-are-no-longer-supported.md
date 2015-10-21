---
title: "Constraint-like `RTCOfferOptions` are no longer supported"
date: "2015-09-09T15:49:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1063808": "Bug 1063808 - createOffer options spec-change to RTCOfferOptions abruptly breaks things in 33"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1064223": "Bug 1064223 - Retire backwards compatible RTCOfferOptions in about 6 weeks"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1197021": "Bug 1197021 - Really retire backwards compatible RTCOfferOptions in 44"
---
The support for deprecated, constraint-like `RTCOfferOptions`, which was once dropped from Firefox 33 but soon restored with warnings for backward compatibility, has been removed from Firefox 43. This old syntax no longer works and logs an error until Firefox 44:

```js
var options = {
    mandatory: { OfferToReceiveAudio: true },
    optional: [{ OfferToReceiveVideo: true }]
};
```

This is the [new syntax](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/WebRTC_basics#options). Watch out for the case difference:

```js
var options = {
    offerToReceiveAudio: true,
    offerToReceiveVideo: true
};
```
