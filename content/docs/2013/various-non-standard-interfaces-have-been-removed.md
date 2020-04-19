---
title: "Various non-standard interfaces have been removed"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
releases: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=899388"
      title: "Bug 899388 – Remove XUL-related interfaces and ChromeWindow from content"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909340"
      title: "Bug 909340 – Hide XULElement from content"
---
As part of the ongoing effort to standardize global objects, the following non-standard [XUL](https://developer.mozilla.org/docs/XUL)-related interfaces have been removed: `ChromeWindow`, `XULButtonElement`, `XULCheckboxElement`, `XULCommandDispatcher`, `XULCommandEvent`, `XULControlElement`, `XULDocument`, `XULElement`, `XULLabeledControlElement`, and `XULPopupElement`.
