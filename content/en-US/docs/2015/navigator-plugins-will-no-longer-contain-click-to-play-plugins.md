---
title: "`navigator.plugins` will no longer contain click-to-play plugins"
date: "2015-10-28T00:29:00-07:00"
categories: ["dom", "plugins"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948": "Bug 1186948 - remove plugins that are click-to-play from navigator.plugins"
---
Plug-ins that have been set to be [click-to-play](https://support.mozilla.org/en-US/kb/why-do-i-have-click-activate-plugins) will be hidden from the [`navigator.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins/plugins) property in the near future.
