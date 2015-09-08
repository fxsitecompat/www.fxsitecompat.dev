---
title: "`HTMLCommandElement` has been dropped"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: "24"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=857116": "Bug 857116 – Remove nsIDOMHTMLCommandElement"
---
The implementation of the obsolete `HTMLCommandElement` interface has been removed in favor of the standardized [`HTMLMenuItemElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMenuItemElement) interface. Firefox has never supported the [`<command>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/command) element, though.
