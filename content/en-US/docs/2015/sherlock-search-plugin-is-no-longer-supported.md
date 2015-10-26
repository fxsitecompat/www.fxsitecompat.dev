---
title: "Sherlock search plugin is no longer supported"
date: "2015-09-23T16:29:00-04:00"
categories: ["misc"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862137": "Bug 862137 - stop supporting Sherlock search engines"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862148": "Bug 862148 - stop supporting installation of Sherlock plugins from the web"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862147": "Bug 862147 - drop support for window.sidebar"
---
The support for the legacy Sherlock search plugin format, [deprecated since Firefox 24](https://www.fxsitecompat.com/en-US/docs/2013/support-for-sherlock-search-plug-ins-has-been-deprecated/), has been dropped with Firefox 44. The [`window.sidebar.addSearchEngine`](https://developer.mozilla.org/en-US/docs/Adding_search_engines_from_web_pages#Installing_Sherlock_plugins) method, that allowed Web pages to invoke an installation of a Sherlock plugin, now just logs a warning in the Web Console. The [`window.external.AddSearchProvider`](https://developer.mozilla.org/en-US/docs/Adding_search_engines_from_web_pages#Installing_OpenSearch_plugins) method can be used instead to offer an [OpenSearch plugin](https://developer.mozilla.org/en-US/Add-ons/Creating_OpenSearch_plugins_for_Firefox).

Note that the support for sidebar panel installation through the `window.sidebar.addPanel` method has already been [removed with Firefox 23](https://www.fxsitecompat.com/en-US/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/). The non-standard [`window.sidebar`](https://developer.mozilla.org/en-US/docs/Web/API/Window/sidebar) object will be completely [removed in the future](https://www.fxsitecompat.com/en-US/docs/2015/window-sidebar-will-be-removed/), though it's still likely used by a number of sites for browser detection. Please do not use this anymore.
