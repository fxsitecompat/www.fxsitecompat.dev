---
title: "`window.find()` dialog support has been dropped"
date: "2017-04-18T17:18:00-04:00"
categories: ["dom"]
tags: []
releases: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672395"
      title: "Bug 672395 - Let's kill window.find()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1348409"
      title: "Bug 1348409 - Assertion failure: XRE_IsParentProcess() with window.find"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/gn4364N4TlY/discussion"
      title: "window.find dialog feature broken in Firefox 53 (a.k.a., Late Intent to Unship: window.find's dialog support)"
---
In Firefox, the [`window.find`](https://developer.mozilla.org/docs/Web/API/Window/find) method could be used to open up a dialog that let the user find strings on the current page. It turns out that the dialog has been broken like [`window.showModalDialog`](https://www.fxsitecompat.dev/en-CA/docs/2016/window-showmodaldialog-has-been-removed/) since the multi-process mode codenamed e10s was enabled with Firefox 48. Starting with Firefox 53, the dialog is broken even when e10s is disabled in the browser.

Given that no other browsers open the Find in Page dialog, Mozilla developers have decided to explicitly remove the support for the `aShowDialog` argument rather than restoring the functionality.

There's also a longstanding plan to remove the non-standard method entirely, so it's discouraged to use it anyway.

**Update**: The `aShowDialog` argument support has been removed with Firefox 53.0.2.
