---
title: "`window.sidebar.addSearchEngine()` has been removed"
date: "2018-01-06T03:47:00-05:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862147"
      title: "Bug 862147 - remove window.external.addSearchEngine"
---
The non-standard `window.sidebar.addSearchEngine` method and its alias `window.external.addSearchEngine` have been removed with Firefox 59. The ability to install legacy Sherlock search plug-ins had already been [removed with Firefox 44](https://www.fxsitecompat.com/en-CA/docs/2015/sherlock-search-plug-ins-are-no-longer-supported/), while [OpenSearch plug-ins](https://developer.mozilla.org/en-US/docs/Web/OpenSearch) can still be installed using the `window.external.AddSearchProvider` method derived from Internet Explorer.

The [`window.sidebar`](https://developer.mozilla.org/en-US/docs/Web/API/Window/sidebar) object is no longer useful so it will also be [removed in the future](https://www.fxsitecompat.com/en-CA/docs/2015/window-sidebar-will-be-removed/).
