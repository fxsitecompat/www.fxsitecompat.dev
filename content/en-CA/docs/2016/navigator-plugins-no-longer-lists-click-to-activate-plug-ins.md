---
title: "`navigator.plugins` no longer lists click-to-activate plug-ins"
date: "2016-06-01T16:39:00-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948"
      title: "Bug 1186948 - remove plugins that are click-to-play from navigator.plugins"
aliases:
    - "/docs/2015/navigator-plugins-will-no-longer-contain-click-to-play-plugins/"
---
Starting with Firefox 49, plug-ins that have been set to [click-to-activate](https://support.mozilla.org/en-US/kb/why-do-i-have-click-activate-plugins) are hidden from [`PluginArray`](https://developer.mozilla.org/en-US/docs/Web/API/PluginArray) returned by the [`navigator.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins/plugins) property. Given that all plug-ins other than Flash are subject to click-to-activate on [Firefox 47](https://www.fxsitecompat.com/en-CA/docs/2016/all-plug-ins-other-than-flash-are-now-defaulted-to-click-to-activate/) and later, "Shockwave Flash" will be the only item listed by default.
