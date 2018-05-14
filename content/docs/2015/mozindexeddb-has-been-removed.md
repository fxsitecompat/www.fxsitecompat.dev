---
title: "`mozIndexedDB` has been removed"
date: "2015-02-27T04:21:22-05:00"
categories: ["dom"]
tags: []
versions: ["38"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=975699"
      title: "Bug 975699 – Remove mozIndexedDB again"
---
The `mozIndexedDB` property, preserved for a [compatibility reason](https://bugzilla.mozilla.org/show_bug.cgi?id=770844), has finally been removed from `window` in favour of the standard [`indexedDB`](https://developer.mozilla.org/docs/Web/API/IDBEnvironment/indexedDB) property.
