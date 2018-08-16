---
title: "`noopener` option for `window.open` no longer affects other window features"
date: "2018-08-16T09:27:00-04:00"
categories: ["dom"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1419960"
      title: "Bug 1419960 - Make the noopener window feature not affect whether other window features are enabled"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6cTk_b1l6LE/discussion"
      title: "Intent to ship: Change the effect of noopener window feature on other window features in window.open"
---
Previously, `window.open(url, '_blank', 'noopener')` would open a new browser window with other [window features](https://developer.mozilla.org/docs/Web/API/Window/open#Window_features) disabled, hiding tabs and back/forward buttons.

Since this seems an unexpected behaviour for users, Firefox 63 and later will treat such code just like `window.open(url, '_blank')` that opens a new browser tab with all window features enabled. The only difference is the new tab's `window.opener` property becoming `null`.

If you want to have certain window features, you should be explicitly specifying these options along with `noopener`.
