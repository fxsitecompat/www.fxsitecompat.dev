---
title: "Flash plug-in content now requires click to activate"
date: "2017-05-17T22:06:00-05:00"
categories: ["plugins"]
tags: []
versions: ["55"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317856"
      title: "Bug 1317856 - Make Flash plugin click-to-play (aka \"Ask to Activate\")"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1365714"
      title: "Bug 1365714 - Release Flash plugin Click-to-Play (aka \"Ask to Activate\")"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1390703"
      title: "Bug 1390703 - Bump Flash Click-to-Play rollout to 25% on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1390705"
      title: "Bug 1390705 - Bump Flash Click-to-Play rollout to 100% on release"
    - url: "https://blog.mozilla.org/futurereleases/2016/07/20/reducing-adobe-flash-usage-in-firefox/"
      title: "Reducing Adobe Flash Usage in Firefox"
aliases:
    - "/en-CA/docs/2016/flash-content-will-be-click-to-activate-in-2017/"
---
As part of the ongoing [NPAPI plug-in deprecation](https://www.fxsitecompat.com/en-CA/categories/plugins/) in Firefox, Flash content is now defaulted to click-to-activate in Firefox Nightly, after some advanced standard technologies including [`SharedArrayBuffer`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SharedArrayBuffer), [WebAssembly](https://developer.mozilla.org/en-US/docs/WebAssembly) and [WebGL 2.0](https://developer.mozilla.org/en-US/docs/Web/API/WebGL2RenderingContext) have been implemented and shipped to public.

The current plan is to roll out this change gradually to the Beta and Release channel user base of Firefox 55. Web publishers must have a clear plan to move away from any Flash dependency to offer the best possible user experience.

**Update**: This change has been rolled out to all Firefox 55 users as of September 20.
