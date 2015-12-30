---
title: "`showModalDialog` has been disabled in multi-process Firefox"
date: "2015-12-29T21:46:00-05:00"
categories: ["dom"]
tags: []
versions: ["46"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1077002": "Bug 1077002 - window.showmodaldialog does not work with e10s"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1234700": "Bug 1234700 - Hide window.showModalDialog, at least when e10s is enabled"
---
The [`window.showModalDialog`](https://developer.mozilla.org/en-US/docs/Web/API/Window/showModalDialog) method is broken and now disabled when Firefox is running in the multi-process mode codenamed [Electrolysis](https://wiki.mozilla.org/Electrolysis) (e10s). The method has been [deprecated since Firefox 28](https://www.fxsitecompat.com/en-US/docs/2013/showmodaldialog-has-been-deprecated/) and will be [completely removed](https://www.fxsitecompat.com/en-US/docs/2015/window-showmodaldialog-will-be-removed/) once e10s, currently enabled by default only on Firefox Nightly and [Developer Edition](https://www.fxsitecompat.com/en-US/docs/2015/multi-process-is-enabled-by-default-on-the-developer-edition/), is enabled on all Firefox channels in mid-2016. 
