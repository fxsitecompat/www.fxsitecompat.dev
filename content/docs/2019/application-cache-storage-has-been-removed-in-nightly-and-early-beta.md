---
title: "Application Cache storage has been removed in Nightly and early Beta"
date: "2019-09-30T17:08:00-04:00"
categories: ["html"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1237782"
      title: "Bug 1237782 - Remove support for appcache storage in Nightly and early beta"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5JqnS_PnKqU/discussion"
      title: "Intent to unship AppCache"
---
The browser storage for HTML5 Application Cache (AppCache), deprecated since [Firefox 44](https://www.fxsitecompat.dev/en-CA/docs/2015/application-cache-api-has-been-deprecated/), is no longer available in the Nightly and early Beta/DevEdition channels starting with Firefox 71. It will be removed from all channels after a few releases. The `applicationCache` property and `OfflineResourceList` interface are still exposed on `window`, but the API will also be removed in the near future. The [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) should be used instead.
