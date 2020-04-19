---
title: "`KeyboardEvent.key` values have been updated for the latest spec"
date: "2015-01-16T09:37:54-05:00"
categories: ["dom"]
tags: []
versions: ["37", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=900372"
      title: "Bug 900372 – Update key names for the latest D3E draft"
---
Some key values returned by the [`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/key) property have been updated for the latest DOM Level 3 Events spec, including `Left`, `Right`, `Del` and `Esc` which have been [deprecated since Firefox 33](https://www.fxsitecompat.dev/en-CA/docs/2014/some-keyboardevent-key-values-have-been-deprecated/). See the [Bug 900372 dependencies](https://bugzilla.mozilla.org/showdependencytree.cgi?id=900372&maxdepth=1&hide_resolved=0) for the changes and the [`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/key) document for a complete list of all possible values.
