---
title: "`getComputedStyle()` no longer returns `null` when style can't be retrieved"
date: "2018-08-15T02:35:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1467722"
      title: "Bug 1467722 - Don't return null from getComputedStyle when there's no presentation."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jh-HAAY1pAQ/discussion"
      title: "Slightly delayed Intent to Ship: getComputedStyle changes on some edge cases."
---
Previously, the [`window.getComputedStyle`](https://developer.mozilla.org/docs/Web/API/Window/getComputedStyle) method was returning `null` or throwing an exception when the style of the given element cannot be retrieved. Such edge cases can be seen with a hidden `<iframe>`, for instance. On Firefox 62 and later, to better align with the CSSOM spec and other browsers' behaviour, the method will return a `CSSStyleDeclaration` object which has `0` for the `length` property and an empty string for every declaration.
