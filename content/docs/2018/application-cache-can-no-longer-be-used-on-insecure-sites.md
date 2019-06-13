---
title: "Application Cache can no longer be used on insecure sites"
date: "2018-05-10T12:54:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460478"
      title: "Bug 1460478 - Disable support for AppCache over insecure contexts for stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qLTTpdzcDkw/discussion"
      title: "Intent to Unship: Application Cache over Insecure Contexts"
    - url: "https://blog.mozilla.org/security/2018/02/12/restricting-appcache-secure-contexts/"
      title: "Mozilla Security Blog: Restricting AppCache to Secure Contexts"
---
Starting with Firefox 62, the [HTML5 Application Cache](https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache) (AppCache) cannot be used any more on non-HTTPS sites, where cache manifest files will be ignored and `window.applicationCache` will be `undefined`. The security restriction has already been introduced to Firefox Nightly and early Beta/DevEdition since the [version 60](https://www.fxsitecompat.dev/en-CA/docs/2018/support-for-application-cache-on-insecure-sites-has-been-deprecated/).

Remember that AppCache has been [deprecated since Firefox 44](https://www.fxsitecompat.dev/en-CA/docs/2015/application-cache-api-has-been-deprecated/) and will be completely [removed in the future](https://www.fxsitecompat.dev/en-CA/docs/2016/application-cache-support-will-be-removed/) in favour of the richer [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API), which only works with HTTPS sites from the beginning.
