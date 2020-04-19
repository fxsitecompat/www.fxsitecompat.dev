---
title: "Pop-up window is now scrollable by default"
date: "2016-05-25T13:52:00-04:00"
categories: ["dom"]
tags: []
versions: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257887"
      title: "Bug 1257887 - Consider changing the default for whether a window opened through window.open() to be scrollable"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1009661"
      title: "Bug 1009661 - Consider ignoring scrollbars=no as a window.open feature for content pages"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/BAmbAhZiR7o/discussion"
      title: "Intent to enable scrollbars by default for windows opened by window.open()"
---
Previously, the `scrollbars` option for [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) was `no` by default. For accessibility reasons, Firefox 49 has changed it to `yes` so that the user is now able to scroll on the newly opened window unless the opener page's author has specified `scrollbars=no` in the method's third argument. Since Chrome and Safari don't honour this option anyway, the compatibility impact should be minimum. Firefox may also ignore the `scrollbars` option in the future.
