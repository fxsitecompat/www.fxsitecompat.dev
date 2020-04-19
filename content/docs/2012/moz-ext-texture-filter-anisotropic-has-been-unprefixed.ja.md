---
title: "`MOZ_EXT_texture_filter_anisotropic` の接頭辞が外れました"
date: "2012-12-03T03:53:26-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=790946"
      title: "Bug 790946 – Remove support for the MOZ_ prefixed EXT_texture_filter_anisotropic ext name"
---
廃止予定となっていた `MOZ_EXT_texture_filter_anisotropic` が削除されました。今後は接頭辞なしの [`EXT_texture_filter_anisotropic`](https://developer.mozilla.org/docs/WebGL/Using_Extensions#EXT_texture_filter_anisotropic) 拡張を使用してください。
