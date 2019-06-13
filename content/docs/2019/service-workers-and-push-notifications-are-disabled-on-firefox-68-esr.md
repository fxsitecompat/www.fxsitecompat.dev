---
title: "Service workers and push notifications are disabled on Firefox 68 ESR"
date: "2019-06-06T23:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1557565"
      title: "Bug 1557565 - Disable Service Workers and push under ESR68 but not under Fennec"
---
The [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) and [Push API](https://developer.mozilla.org/docs/Web/API/Push_API) will remain disabled on Firefox 68 [Extended Support Release](https://www.mozilla.org/firefox/organizations/) (ESR), as with [Firefox 45](https://www.fxsitecompat.dev/en-CA/docs/2016/service-workers-have-been-disabled-in-firefox-45-esr/), [Firefox 52](https://www.fxsitecompat.dev/en-CA/docs/2017/service-workers-and-push-notifications-are-disabled-on-firefox-52-esr/) and [Firefox 60](https://www.fxsitecompat.dev/en-CA/docs/2018/service-workers-and-push-notifications-are-disabled-on-firefox-60-esr/) ESRs, because of the continuing architectural changes to properly support multiple content processes in the browser. Firefox ESR is mainly for mass deployment in large companies and universities. Those APIs are available for regular Release channel users as well as on Android.
