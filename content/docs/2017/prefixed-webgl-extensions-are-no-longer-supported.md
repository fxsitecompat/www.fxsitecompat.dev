---
title: "Prefixed WebGL extensions are no longer supported"
date: "2017-11-08T16:43:00-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403413"
      title: "Bug 1403413 - Remove deprecated MOZ_ extension prefix aliases"
---
The support for the following prefixed [WebGL extension](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API/Using_Extensions) aliases, deprecated for years since [Firefox 27](https://www.fxsitecompat.com/en-CA/docs/2013/prefixed-extensions-have-been-deprecated/), has been removed with Firefox 58. Use the standard extensions instead.

* `MOZ_WEBGL_lose_context`
* `MOZ_WEBGL_compressed_texture_s3tc`
* `MOZ_WEBGL_compressed_texture_atc`
* `MOZ_WEBGL_compressed_texture_pvrtc`
* `MOZ_WEBGL_depth_texture`
