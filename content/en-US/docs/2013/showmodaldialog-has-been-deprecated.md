---
title: "`showModalDialog` has been deprecated"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
versions: ["28"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=933040": "Bug 933040 – Warn for showModalDialog uses"
---
The [`window.showModalDialog`](https://developer.mozilla.org/en-US/docs/Web/API/window.showModalDialog) method, originally from Internet Explorer, is now considered deprecated. The [`window.open`](https://developer.mozilla.org/en-US/docs/Web/API/window.open) method should be used instead.

**Update**: The method has been [disabled since Firefox 46](https://www.fxsitecompat.com/en-US/docs/2015/showmodaldialog-has-been-disabled-in-multi-process-firefox/) when Firefox is running in the multi-process mode.
