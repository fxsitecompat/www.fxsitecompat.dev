---
title: "`::selection` pseudo-element has been unprefixed"
date: "2018-05-10T12:36:00-04:00"
categories: ["css"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=509958"
      title: "Bug 509958 - Remove the -moz prefix from ::selection"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/dQVpQYjn3-M/discussion"
      title: "Intent to unprefix: ::-moz-selection."
---
The [`::selection`](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection) pseudo-element has been unprefixed with Firefox 62. Firefox was the only major browser retaining the vendor prefix. The deprecated `::-moz-selection` is still available as an alias but will be removed in the future.
