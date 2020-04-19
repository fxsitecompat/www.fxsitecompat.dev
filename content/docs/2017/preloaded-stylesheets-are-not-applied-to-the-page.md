---
title: "Preloaded stylesheets are not applied to the page"
date: "2017-10-24T19:10:00-04:00"
categories: ["css"]
tags: []
releases: ["56", "60-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1405761"
      title: "Bug 1405761 - css not loaded correctly with rel=preload"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/aNUUx0S6PxE/discussion"
      title: "Intent to unship: rel=preload for firefox 57"
aliases:
    - "/en-CA/docs/2017/css-loaded-with-link-rel-preload-are-not-applied/"
---
Firefox 56 has added the support for [preloading content](https://developer.mozilla.org/docs/Web/HTML/Preloading_content) with `<link rel="preload">` for a better web performance. However, there have been reports of preloaded CSS stylesheets not applied to the HTML document properly. For that reason, this new feature will be temporarily disabled in Firefox 57 while Mozilla developers are working on the solution, and is planned to be re-enabled with Firefox 58 coming January 2018.
