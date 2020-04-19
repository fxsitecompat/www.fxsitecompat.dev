---
title: "Service workers and push notifications are disabled on Firefox 52 ESR"
date: "2017-02-09T16:58:00-05:00"
categories: ["dom"]
tags: []
releases: ["52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1338144"
      title: "Bug 1338144 - disable service workers and push notifications on 52 ESR"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/TWE4VEbJOmM/discussion"
      title: "Intent to disable service workers and push in 52 ESR"
---
The [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) and [Push API](https://developer.mozilla.org/docs/Web/API/Push_API) will be disabled on Firefox 52 [Extended Support Release](https://www.mozilla.org/firefox/organizations/) (ESR), as with [Firefox 45 ESR](https://www.fxsitecompat.dev/en-CA/docs/2016/service-workers-have-been-disabled-in-firefox-45-esr/), due to the upcoming major architectural changes to support multiple content processes in the browser. Firefox 52 ESR is mainly for enterprise users as well as [Windows XP/Vista users](https://support.mozilla.org/kb/end-support-windows-xp-and-vista) who cannot upgrade to Firefox 53 and later. Those APIs are available for regular Release channel users.

**Update**: Those APIs are still [disabled in Firefox 60 ESR](https://www.fxsitecompat.dev/en-CA/docs/2018/service-workers-and-push-notifications-are-disabled-on-firefox-60-esr/).
