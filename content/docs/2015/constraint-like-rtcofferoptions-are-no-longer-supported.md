---
title: "Constraint-like `RTCOfferOptions` are no longer supported"
date: "2015-09-09T15:49:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["43", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1063808"
      title: "Bug 1063808 - createOffer options spec-change to RTCOfferOptions abruptly breaks things in 33"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1064223"
      title: "Bug 1064223 - Retire backwards compatible RTCOfferOptions in about 6 weeks"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1197021"
      title: "Bug 1197021 - Really retire backwards compatible RTCOfferOptions in 44"
---
The support for deprecated, constraint-like `RTCOfferOptions`, which was once dropped from Firefox 33 but soon restored with warnings for backward compatibility, has been removed from Firefox 43. This old syntax no longer works and logs an error until Firefox 44:

```js
var options = {
    mandatory: { OfferToReceiveAudio: true },
    optional: [{ OfferToReceiveVideo: true }]
};
```

This is the [new syntax](https://developer.mozilla.org/docs/Web/API/WebRTC_API/WebRTC_basics#options). Watch out for the case difference:

```js
var options = {
    offerToReceiveAudio: true,
    offerToReceiveVideo: true
};
```
