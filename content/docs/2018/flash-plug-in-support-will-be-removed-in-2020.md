---
title: "Flash plug-in support will be removed in 2020"
date: "2018-06-05T15:17:00-04:00"
categories: ["plugins"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455897"
      title: "Bug 1455897 - Remove support for the Flash plugin when Flash EOL's per the roadmap"
---
In July 2017, [Adobe Systems](https://theblog.adobe.com/adobe-flash-update/) announced that the Flash Player plug-in would reach the end-of-life by the end of 2020, and [Mozilla](https://blog.mozilla.org/futurereleases/2017/07/25/firefox-roadmap-flash-end-life/) among other browser vendors updated the [Flash support roadmap](https://developer.mozilla.org/docs/Plugins/Roadmap) at the same time.

According to the current timeline, Firefox starts showing a user-visible warning on sites using Flash in early 2019, and Flash Player will be disabled by default a few months later. Then Firefox will completely remove the plug-in support in early 2020, while Firefox Extended Support Release (ESR) for organizations will maintain the support until the end of 2020.

Firefox for desktop has dropped the support for all other [NPAPI plug-ins](https://www.fxsitecompat.com/en-CA/categories/plugins/) by the release of [Firefox 52](https://www.fxsitecompat.com/en-CA/docs/2016/plug-in-support-has-been-dropped-other-than-flash/). Firefox for Android has already removed the Flash support with [Firefox 56](https://www.fxsitecompat.com/en-CA/docs/2017/flash-plug-in-is-no-longer-supported-by-firefox-for-android/). Firefox for iOS is WebKit-based so it has never supported browser plug-ins.

Websites still relying on Flash should have a solid migration plan not to miss the deadline. The [Flash to HTML5 migration guide](https://developer.mozilla.org/docs/Plugins/Flash_to_HTML5) on MDN provides more information about this topic.
