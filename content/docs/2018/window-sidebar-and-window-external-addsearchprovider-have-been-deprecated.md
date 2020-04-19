---
title: "`window.sidebar` and `window.external.AddSearchProvider()` have been deprecated"
date: "2018-10-31T22:32:00-04:00"
categories: ["dom"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503551"
      title: "Bug 1503551 - Make window.external.AddSearchProvider a dummy function"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1512047"
      title: "Bug 1512047 - Can not add more search engines from AMO"
---
The non-standard, Netscape-derived [`window.sidebar`](https://developer.mozilla.org/docs/Web/API/window.sidebar) object, an alias of `window.external`, is now officially considered deprecated and will be [removed in the future](https://www.fxsitecompat.dev/en-CA/docs/2015/window-sidebar-will-be-removed/). The object is no longer available on the Nightly channel as of Firefox 65. Web developers must stop using it for browser detection.

The IE-derived `window.external` object will remain, but the `AddSearchProvider` and `IsSearchProviderInstalled` methods on it will be no-op, simply returning `undefined`, according to the latest HTML spec. This change has also been made to Firefox 65 Nightly. While `AddSearchProvider` could be used to add an OpenSearch plug-in to the browser, `IsSearchProviderInstalled` was always returning `0` on Firefox.

There is no plan to remove the [auto-discovery of search plug-ins](https://developer.mozilla.org/docs/Web/OpenSearch#Autodiscovery_of_search_plugins) via `<link rel="search">`, which is a recommended way to provide an OpenSearch plug-in on a website.

**Update**: Firefox 66 Nightly has re-enabled `window.sidebar` and these methods as Firefox developers are thinking about a plan to migrate the search provider installer.
