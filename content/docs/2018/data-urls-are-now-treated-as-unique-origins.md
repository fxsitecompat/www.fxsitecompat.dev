---
title: "Data URLs are now treated as unique origins"
date: "2018-01-24T10:37:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["57"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1324406"
      title: "Bug 1324406 - Treat 'data:' documents as unique, opaque origins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1418639"
      title: "Bug 1418639 - Page doesn't work in FF57 due to Firefox-only use of data: URIs by YUI library"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/A7LO5c6y3j4/discussion"
      title: "Intent to ship: Treating 'data:' documents as unique, opaque origins"
    - url: "https://blog.mozilla.org/security/2017/10/04/treating-data-urls-unique-origins-firefox-57/"
      title: "Mozilla Security Blog: Treating data URLs as unique origins for Firefox 57"
---
Starting with Firefox 57, [data URLs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs) prefixed with the `data:` scheme will be treated as unique [origins](https://developer.mozilla.org/en-US/docs/Glossary/Origin). It means the scripts within data URLs loaded in an `<iframe>` are no longer able to access the embedding page's objects. This change is aimed at not only mitigating the risk of cross-site scripting (XSS) attacks but also aligning Firefox with the HTML standard as well as the behaviour of other browsers.

The rich text editor functionality in *YUI 2* is known to be broken because it uses data URLs only for Firefox. Given that the library is no longer actively maintained, the users should consider migrating to any promising alternative. So far Mozilla has no plan to solve the issue in the Firefox side.
