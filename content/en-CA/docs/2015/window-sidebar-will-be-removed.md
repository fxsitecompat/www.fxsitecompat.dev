---
title: "`window.sidebar` will be removed"
date: "2015-10-25T22:07:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862147"
      title: "Bug 862147 - drop support for window.sidebar"
---
The deprecated, non-standard [`window.sidebar`](https://developer.mozilla.org/en-US/docs/Web/API/window.sidebar) object will be removed in the near future. The `addPanel` method has been [removed with Firefox 23](https://www.fxsitecompat.com/en-CA/docs/2013/ability-to-add-a-sidebar-panel-has-been-dropped/), and `addSearchEngine` method has [dropped the Sherlock support with Firefox 44](https://www.fxsitecompat.com/en-CA/docs/2015/sherlock-search-plug-ins-are-no-longer-supported/), so this object is no longer useful. However, apparently it's still used by some sites for browser detection. Web developers should stop using it.
