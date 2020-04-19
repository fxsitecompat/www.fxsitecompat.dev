---
title: "Prefixed extensions have been deprecated"
date: "2013-10-08T20:15:35-04:00"
categories: ["canvas-webgl"]
tags: []
releases: ["27", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=924176"
      title: "Bug 924176 – Warn on prefixed WebGL extensions usage (deprecated)"
---
`MOZ_` prefixed WebGL [extension strings](https://developer.mozilla.org/docs/Web/WebGL/Using_Extensions) are now deprecated. Support for them will be removed in the future. Use unprefixed extension strings instead.

* **Update**: The prefixed aliases have been removed with [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/prefixed-webgl-extensions-are-no-longer-supported/).
