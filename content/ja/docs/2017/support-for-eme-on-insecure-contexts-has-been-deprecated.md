---
title: "安全でないコンテキスト上での EME 対応が廃止予定となりました"
date: "2017-05-04T17:21:00-04:00"
categories: ["audio-video"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1322517"
      title: "Bug 1322517 - [EME] Remove support for EME on insecure contexts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1361000"
      title: "Bug 1361000 - Add deprecation warning for removing support for EME on insecure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/sa_2q8oEKgE/discussion"
      title: "Intent to remove: Insecure use of Encrypted Media Extensions"
---
[Encrypted Media Extensions (EME) API](https://developer.mozilla.org/ja/docs/Web/API/Encrypted_Media_Extensions_API) は、*Netflix* のようなパブリッシャーによって DRM 保護付きコンテンツの配信に使われていますが、最新の仕様によれば [安全なコンテキスト](https://developer.mozilla.org/ja/docs/Web/Security/Secure_Contexts) 上でのみ使用可能とされています。Firefox では、安全でないコンテキスト上での EME 対応はコンソールへの警告を伴って廃止予定となり、近い将来削除されます。
