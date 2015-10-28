---
title: "`window.showModalDialog` will be removed"
date: "2015-10-27T22:25:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=981796": "Bug 981796 - Remove window.showModalDialog"
---
The [`window.showModalDialog`](https://developer.mozilla.org/en-US/docs/Web/API/Window/showModalDialog) method, [deprecated since Firefox 28](https://www.fxsitecompat.com/en-US/docs/2013/showmodaldialog-has-been-deprecated/) will be removed in the near future. Use the standard [`window.open`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open) method or a custom in-page modal UI instead. The HTML5 [`<dialog>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog) element is another replacement but is not implemented in Firefox yet.
