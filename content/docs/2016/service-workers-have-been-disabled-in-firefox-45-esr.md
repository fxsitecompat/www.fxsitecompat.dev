---
title: "Service Workers have been disabled in Firefox 45 ESR"
date: "2016-03-07T10:52:00-05:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1232029"
      title: "Bug 1232029 - disable service workers in 45 ESR"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/yuNHtDhl3lY/discussion"
      title: "Intent to disable service workers in 45 ESR"
---
The [Service Worker API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API), shipped with Firefox 44, has been disabled in Firefox 45 [Extended Support Release](https://www.mozilla.org/firefox/organizations/) (ESR). Both the spec and implementation are likely to change in 2016, therefore offering the API on the stable ESR channel might lead to site compatibility issues. The API is still available on other channels.

**Update**: Those APIs are still [disabled in Firefox 52 ESR](https://www.fxsitecompat.com/en-CA/docs/2017/service-workers-and-push-notifications-are-disabled-on-firefox-52-esr/).

**Update 2**: Those APIs are still [disabled in Firefox 60 ESR](https://www.fxsitecompat.com/en-CA/docs/2018/service-workers-and-push-notifications-are-disabled-on-firefox-60-esr/).
