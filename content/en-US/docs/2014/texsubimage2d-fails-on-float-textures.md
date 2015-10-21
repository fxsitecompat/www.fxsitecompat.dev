---
title: "`texSubImage2D` fails on float textures"
date: "2014-02-07T11:57:09-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["29", "30"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1003607": "Bug 1003607 – Header animation at acko.net is broken in FF 29 and above."
---
The `texSubImage2D` method on the [`WebGLRenderingContext`](https://developer.mozilla.org/en-US/docs/Web/API/WebGLRenderingContext) interface fails when it is used to update float textures created with the `OES_texture_float` extension, throwing an error: "format or type doesn't match the existing texture". This issue has been fixed with Firefox 31.
