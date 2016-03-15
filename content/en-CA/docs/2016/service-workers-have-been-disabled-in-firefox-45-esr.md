---
title: "Service Workers have been disabled in Firefox 45 ESR"
date: "2016-03-07T10:52:00-05:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1232029"
      title: "Bug 1232029 - disable service workers in 45 ESR"
---
The [Service Worker API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API), shipped with Firefox 44, has been disabled in Firefox 45 [Extended Support Release](https://www.mozilla.org/en-US/firefox/organizations/) (ESR). Both the spec and implementation are likely to change in 2016, therefore offering the API on the stable ESR channel might lead to site compatibility issues. The API is still available on other channels.
