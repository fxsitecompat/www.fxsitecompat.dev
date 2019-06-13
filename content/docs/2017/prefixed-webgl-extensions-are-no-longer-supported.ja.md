---
title: "接頭辞付き WebGL 拡張機能の対応が打ち切られました"
date: "2017-11-08T16:43:00-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403413"
      title: "Bug 1403413 - Remove deprecated MOZ_ extension prefix aliases"
---
[Firefox 27](https://www.fxsitecompat.dev/ja/docs/2013/prefixed-extensions-have-been-deprecated/) 以降何年間も廃止予定となっていた以下の接頭辞付き [WebGL 拡張機能](https://developer.mozilla.org/docs/Web/API/WebGL_API/Using_Extensions) エイリアスへの対応は Firefox 58 で削除されました。標準の拡張機能で代用してください。

* `MOZ_WEBGL_lose_context`
* `MOZ_WEBGL_compressed_texture_s3tc`
* `MOZ_WEBGL_compressed_texture_atc`
* `MOZ_WEBGL_compressed_texture_pvrtc`
* `MOZ_WEBGL_depth_texture`
