---
title: "`navigator.plugins` no longer lists Flash when it's click-to-activate"
date: "2016-06-01T16:39:00-04:00"
categories: ["dom", "plugins"]
tags: []
versions: ["49"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948"
      title: "Bug 1186948 - remove Flash from navigator.plugins when it's click-to-play"
aliases:
    - "/docs/2015/navigator-plugins-will-no-longer-contain-click-to-play-plugins/"
    - "/docs/2016/navigator-plugins-no-longer-lists-click-to-activate-plug-ins/"
---
Starting with Firefox 49, the Adobe Flash Player plug-in will be hidden from [`PluginArray`](https://developer.mozilla.org/en-US/docs/Web/API/PluginArray) returned by the [`navigator.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins/plugins) property when it has been set to [click-to-activate](https://developer.mozilla.org/en-US/Add-ons/Plugins/Site_Author_Guide_for_Click-To-Activate_Plugins). Since many sites are falling back to HTML5 video when Flash could not be detected, this change is supposed to improve the user experience where the plug-in had to be activated manually. Other plug-ins are not affected at this time.

**Update**: This change was reverted just before it goes to the Aurora channel (Developer Edition) due to the [broken Flash activation](https://bugzilla.mozilla.org/show_bug.cgi?id=1277832) as well as video playback not working on [*Hulu*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277760) and [*Facebook*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277825). Mozilla developers are investigating those issues.
