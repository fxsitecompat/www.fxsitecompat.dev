---
title: "Support for application cache on insecure sites has been deprecated"
date: "2018-02-02T01:29:00-05:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["60", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1354175"
      title: "Bug 1354175 - Remove access to AppCache in insecure contexts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/qLTTpdzcDkw/discussion"
      title: "Intent to Unship: Application Cache over Insecure Contexts"
    - url: "https://blog.mozilla.org/security/2018/02/12/restricting-appcache-secure-contexts/"
      title: "Mozilla Security Blog: Restricting AppCache to Secure Contexts"
---
As part of the ongoing [insecure HTTP deprecation](https://www.fxsitecompat.dev/en-CA/docs/2015/insecure-http-will-be-deprecated/), Firefox 60 Nightly and early Beta/DevEdition will no longer allow non-HTTPS sites to use the application cache (AppCache). When disabled, cache manifest files will be ignored and `window.applicationCache` will be `undefined`. Assuming no major issues arise, Firefox 62 will make the change on all the channels.

Note that the AppCache support itself has also been [deprecated since Firefox 44](https://www.fxsitecompat.dev/en-CA/docs/2015/application-cache-api-has-been-deprecated/) and will be completely [removed in the future](https://www.fxsitecompat.dev/en-CA/docs/2016/application-cache-support-will-be-removed/) in favour of the richer Service Worker API.

**Update**: As planned, all the channels impose the restriction as of [Firefox 62](https://www.fxsitecompat.dev/en-CA/docs/2018/application-cache-can-no-longer-be-used-on-insecure-sites/).
