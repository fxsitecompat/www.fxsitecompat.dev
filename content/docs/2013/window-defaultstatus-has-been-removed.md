---
title: "`window.defaultStatus` has been removed"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862917"
      title: "Bug 862917 – Remove window.defaultStatus"
---
The [`window.defaultStatus`](https://developer.mozilla.org/docs/Web/API/window.defaultStatus) property is no longer available. Setting this property has had no effect in Firefox because the default preference has disallowed changes to the status text by Web pages. Recently, the Firefox UI dropped support for enabling that pref. Also, this property is not specified in the HTML5 spec. [`window.status`](https://developer.mozilla.org/docs/Web/API/window.status) is still available.
