---
title: "`HTMLCommandElement` has been dropped"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
releases: ["24", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=857116"
      title: "Bug 857116 – Remove nsIDOMHTMLCommandElement"
---
The implementation of the obsolete `HTMLCommandElement` interface has been removed in favour of the standardized [`HTMLMenuItemElement`](https://developer.mozilla.org/docs/Web/API/HTMLMenuItemElement) interface. Firefox has never supported the [`<command>`](https://developer.mozilla.org/docs/Web/HTML/Element/command) element, though.
