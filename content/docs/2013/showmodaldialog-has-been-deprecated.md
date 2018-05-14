---
title: "`showModalDialog` has been deprecated"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
versions: ["28"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=933040"
      title: "Bug 933040 – Warn for showModalDialog uses"
---
The [`window.showModalDialog`](https://developer.mozilla.org/docs/Web/API/window.showModalDialog) method, originally from Internet Explorer, is now considered deprecated. The [`window.open`](https://developer.mozilla.org/docs/Web/API/window.open) method should be used instead.

**Update**: The method has been [disabled since Firefox 46](https://www.fxsitecompat.com/en-CA/docs/2015/showmodaldialog-has-been-disabled-in-multi-process-firefox/) when Firefox is running in the multi-process mode dubbed *e10s*.

**Update**: The method is no longer available on [Firefox 48](https://www.fxsitecompat.com/en-CA/docs/2016/window-showmodaldialog-has-been-removed/) and later as *e10s* has been enabled by default.
