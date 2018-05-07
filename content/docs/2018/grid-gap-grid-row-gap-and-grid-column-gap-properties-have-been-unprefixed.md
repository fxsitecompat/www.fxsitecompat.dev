---
title: "`grid-gap`, `grid-row-gap` and `grid-column-gap` properties have been unprefixed"
date: "2018-05-07T13:51:00-04:00"
categories: ["css"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398482"
      title: "Bug 1398482 - [css-grid] Drop the \"grid-\" prefix from the grid-gap, grid-row-gap, and grid-column-gap properties"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/InRVDzXKbkM/discussion"
      title: "Intent to unprefix grid-gap, grid-row-gap, and grid-column-gap and updating them to spec"
---
Firefox 61 has dropped the `grid` prefix from the [`grid-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-gap), [`grid-row-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row-gap) and [`grid-column-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column-gap) properties as per the latest CSS Grid Layout Module spec, so those are now `gap`, `row-gap` and `column-gap` respectively. The old prefixed properties can still be used as aliases but will be removed in the future.
