---
title: "`moz-webgl` context requests are no longer supported"
date: "2014-02-07T11:57:09-05:00"
categories: ["canvas-webgl"]
tags: []
versions: ["29"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=913597"
      title: "Bug 913597 – Remove support for \'moz-webgl\' context requests"
---
The support for retrieving a [WebGL](https://developer.mozilla.org/docs/Web/WebGL) context from a [Canvas](https://developer.mozilla.org/docs/HTML/Canvas) using the obsolete `moz-webgl` name has been removed. Use the standard `webgl` context instead as described in [Getting started with WebGL](https://developer.mozilla.org/docs/Web/WebGL/Getting_started_with_WebGL#Creating_a_WebGL.C2.A0context).
