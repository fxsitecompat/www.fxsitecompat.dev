---
title: "`MediaKeySession.keySystem` has been removed"
date: "2017-04-24T01:20:00-04:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["54", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1016162"
      title: "Bug 1016162 - [EME] Encrypted Media Extensions base DOM API"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335555"
      title: "Bug 1335555 - [EME] Remove MediaKeySession.keySystem"
---
The `keySystem` property on the [`MediaKeySession`](https://developer.mozilla.org/docs/Web/API/MediaKeySession) interface, implemented initially with Firefox 32 as part of the [Encrypted Media Extensions API](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API), has been removed as it's no longer in the spec. [`MediaKeySystemAccess.keySystem`](https://developer.mozilla.org/docs/Web/API/MediaKeySystemAccess/keySystem) should be used instead.
