---
title: "`offset-*` logical properties have been renamed to `inset-*`"
date: "2018-08-15T02:08:00-04:00"
categories: ["css"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1464782"
      title: "Bug 1464782 - [css-logical] rename offset-* properties to inset-block-start, inset-block-end, inset-inline-start and inset-inline-end"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1471838"
      title: "Bug 1471838 - Turn layout.css.offset-logical-properties.enabled off by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/mG6Wpz5C2PM/discussion"
      title: "Intent to deprecate and remove: offset-* logical properties."
---
Firefox 63 has renamed the following logical properties according to the latest CSS Logical Properties and Values spec. Given that these are implemented only in Firefox and not yet widely used so far, this change has been made with no transition period.

* `offset-block-start` → [`inset-block-start`](https://developer.mozilla.org/docs/Web/CSS/inset-block-start)
* `offset-block-end` → [`inset-block-end`](https://developer.mozilla.org/docs/Web/CSS/inset-block-end)
* `offset-inline-start` → [`inset-inline-start`](https://developer.mozilla.org/docs/Web/CSS/inset-inline-start)
* `offset-inline-end` → [`inset-inline-end`](https://developer.mozilla.org/docs/Web/CSS/inset-inline-end)
