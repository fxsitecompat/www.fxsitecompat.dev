---
title: "Service workers and push notifications are disabled on Firefox 60 ESR"
date: "2018-05-06T18:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457915"
      title: "Bug 1457915 - disable service workers and push notification on 60 ESR"
---
The [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) and [Push API](https://developer.mozilla.org/docs/Web/API/Push_API) will be disabled on Firefox 60 [Extended Support Release](https://www.mozilla.org/firefox/organizations/) (ESR), as with [Firefox 45](https://www.fxsitecompat.dev/en-CA/docs/2016/service-workers-have-been-disabled-in-firefox-45-esr/) and [Firefox 52](https://www.fxsitecompat.dev/en-CA/docs/2017/service-workers-and-push-notifications-are-disabled-on-firefox-52-esr/) ESRs, because of the continuing architectural changes to properly support multiple content processes in the browser. Firefox ESR is mainly for mass deployment in large companies and universities. Those APIs are available for regular Release channel users.
