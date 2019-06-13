---
title: "Some Flash content is broken due to async rendering mode"
date: "2016-10-24T09:51:00-04:00"
categories: ["plugins"]
tags: []
versions: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1229961"
      title: "Bug 1229961 - Enable direct plugin drawing by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305135"
      title: "Bug 1305135 - Flash 23 isn't using async rendering mode on release channels"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1307108"
      title: "Bug 1307108 - Enable async rendering by default on 49 using a system addon"
---
[Firefox 49.0.2](https://www.mozilla.org/firefox/49.0.2/releasenotes/) has enabled asynchronous rendering of the Adobe Flash Player plug-in by default, aiming to improve the browser's stability and performance. It also solves the known issues on 64-bit Windows about [Stage 3D support](https://www.fxsitecompat.dev/en-CA/docs/2016/flash-is-forced-windowless-mode-on-firefox-for-64-bit-windows-affecting-stage-3d/), [input method editors (IMEs)](https://bugzilla.mozilla.org/show_bug.cgi?id=1301486) and page scrolling.

There are, however, [reports of various broken content](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1229961&maxdepth=1&hide_resolved=0) including video players and games. Mozilla developers are investigating those issues.

**Update**: Due to considerable regressions, the async plug-in rendering will soon be [disabled remotely](https://bugzilla.mozilla.org/show_bug.cgi?id=1312528) on the Window 32-bit version of Firefox 49. It has also been disabled on Firefox 50 Beta. Meanwhile on the 64-bit version, it will remain enabled to avoid the issues mentioned above.
