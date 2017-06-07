---
title: "`window.showModalDialog` has been removed"
date: "2016-06-08T09:07:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=981796"
      title: "Bug 981796 - Remove window.showModalDialog"
    - url: "https://asadotzler.com/2016/06/06/firefox-48-beta-release-and-e10s/"
      title: "Firefox 48 Beta, Release, and E10S"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/4t5AAxxrCoA/discussion"
      title: "Intent to unship: window.showModalDialog"
aliases:
    - "/docs/2015/window-showmodaldialog-will-be-removed/"
---
The legacy [`window.showModalDialog`](https://developer.mozilla.org/en-US/docs/Web/API/Window/showModalDialog) method, [deprecated since Firefox 28](https://www.fxsitecompat.com/en-CA/docs/2013/showmodaldialog-has-been-deprecated/) and [disabled since Firefox 46](https://www.fxsitecompat.com/en-CA/docs/2015/showmodaldialog-has-been-disabled-in-multi-process-firefox/) when the browser is running in the multi-process mode dubbed *e10s*, is no longer available on Firefox 48 and later as *e10s* has been enabled by default.

Not all Firefox users will benefit from *e10s* as of the release of Firefox 48, and technically the method still exists when *e10s* is disabled. However, given that it's practically gone, you should be using the standard [`window.open`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open) method or a custom in-page modal UI instead. In the latter case, it is recommended to implement the WAI-ARIA [`dialog` role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_dialog_role) to ensure the accessibility. Unfortunately the HTML [`<dialog>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog) element is not yet implemented in Firefox.
