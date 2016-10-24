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
[Firefox 49.0.2](https://www.mozilla.org/en-US/firefox/49.0.2/releasenotes/) has enabled asynchronous rendering of the Adobe Flash Player plug-in by default, aiming to improve the browser's stability and performance. It also solves the known issues on [Stage 3D support on 64-bit Windows](https://www.fxsitecompat.com/en-CA/docs/2016/flash-is-forced-windowless-mode-on-firefox-for-64-bit-windows-affecting-stage-3d/) and [input method editors (IMEs)](https://bugzilla.mozilla.org/show_bug.cgi?id=1301486).

There are, however, [reports of various broken content](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1229961&maxdepth=1&hide_resolved=0) including video players and games. Mozilla developers are investigating those issues.
