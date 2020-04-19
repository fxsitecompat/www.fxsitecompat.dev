---
title: "`MediaKeySession.keySystem` が削除されました"
date: "2017-04-24T01:20:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1016162"
      title: "Bug 1016162 - [EME] Encrypted Media Extensions base DOM API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335555"
      title: "Bug 1335555 - [EME] Remove MediaKeySession.keySystem"
---
当初 Firefox 32 で [Encrypted Media Extensions API](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) の一部として実装された [`MediaKeySession`](https://developer.mozilla.org/docs/Web/API/MediaKeySession) インターフェイス上の `keySystem` プロパティは、現行仕様に含まれていないことから削除されました。[`MediaKeySystemAccess.keySystem`](https://developer.mozilla.org/docs/Web/API/MediaKeySystemAccess/keySystem) を代わりに使用してください。
