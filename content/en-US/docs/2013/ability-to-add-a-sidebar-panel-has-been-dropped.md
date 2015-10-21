---
title: "Ability to add a sidebar panel has been dropped"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=691647": "Bug 691647 – clean up nsISidebar (remove window.sidebar.addPanel/addPersistentPanel)"
---
`window.sidebar.addPanel` and `window.sidebar.addPersistentPanel` are no longer supported. These methods were a part of a Netscape-derived API which allowed Web publishers to integrate their contents as sidebar panels of the browser. They were not standardized, rarely used, and not very well supported. No other browsers have implemented these.

There is also a [plan](https://bugzilla.mozilla.org/show_bug.cgi?id=862147) to remove [`window.sidebar`](https://developer.mozilla.org/en-US/docs/Web/API/window.sidebar) itself in the future.

As alternatives to those API, you can [create a sidebar extension or utilize the Social API](https://developer.mozilla.org/en-US/docs/Creating_a_Firefox_sidebar).
