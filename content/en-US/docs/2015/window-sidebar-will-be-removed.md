---
title: "`window.sidebar` will be removed"
date: "2015-10-25T22:07:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=862147": "Bug 862147 - drop support for window.sidebar"
---
The deprecated, non-standard [`window.sidebar`](https://developer.mozilla.org/en-US/docs/Web/API/window.sidebar) object will be removed in the near future. The [`addPanel`](https://www.fxsitecompat.com/en-US/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/) and [`addSearchEngine`](https://www.fxsitecompat.com/en-US/docs/2015/sherlock-search-plugin-is-no-longer-supported/) methods have been removed with Firefox 23 and 44 respectively, so the object is no longer useful. However, apparently it's still used by some sites for browser detection. Web developers should stop using it.
