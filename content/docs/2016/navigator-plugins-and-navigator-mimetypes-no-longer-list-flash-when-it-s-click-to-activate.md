---
title: "`navigator.plugins` and `navigator.mimeTypes` no longer list Flash when it's click-to-activate"
date: "2016-06-30T17:20:00-04:00"
categories: ["dom", "plugins"]
tags: []
releases: ["50"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186948"
      title: "Bug 1186948 - remove Flash from navigator.plugins when it's click-to-play"
aliases:
    - "/en-CA/docs/2015/navigator-plugins-will-no-longer-contain-click-to-play-plugins/"
    - "/en-CA/docs/2016/navigator-plugins-no-longer-lists-click-to-activate-plug-ins/"
    - "/en-CA/docs/2016/navigator-plugins-no-longer-lists-flash-when-it-s-click-to-activate/"
---
Starting with Firefox 50, Adobe Flash Player will be hidden from the [`navigator.plugins`](https://developer.mozilla.org/docs/Web/API/NavigatorPlugins/plugins) and [`navigator.mimeTypes`](https://developer.mozilla.org/docs/Web/API/NavigatorPlugins/mimeTypes) properties when the plug-in has been set to [click-to-activate](https://developer.mozilla.org/Add-ons/Plugins/Site_Author_Guide_for_Click-To-Activate_Plugins). Since many sites are falling back to HTML5 video when Flash could not be detected, this change is supposed to improve the user experience where the plug-in had to be activated manually. Other plug-ins remain the same at this time.

**Update**: This change was reverted just before it goes to the Aurora channel (Firefox 49 Developer Edition) due to the [broken Flash activation](https://bugzilla.mozilla.org/show_bug.cgi?id=1277832) as well as video playback not working on [*Hulu*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277760) and [*Facebook*](https://bugzilla.mozilla.org/show_bug.cgi?id=1277825). Mozilla developers are investigating those issues.

**Update**: The bug described above has been fixed and the patch has been re-landed to Firefox 50. We have updated this document to explain `navigator.mimeTypes` is also affected.

**Update**: This change was [disabled](https://bugzilla.mozilla.org/show_bug.cgi?id=1296004) during the Aurora development cycle due to a couple of plug-in activation bugs.
