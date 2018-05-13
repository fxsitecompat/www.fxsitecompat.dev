---
title: "`grid-gap`、`grid-row-gap`、`grid-column-gap` プロパティの接頭辞が外れました"
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
最新の CSS Grid Layout Module 仕様に従い、Firefox 61 で [`grid-gap`](https://developer.mozilla.org/docs/Web/CSS/grid-gap)、[`grid-row-gap`](https://developer.mozilla.org/docs/Web/CSS/grid-row-gap)、[`grid-column-gap`](https://developer.mozilla.org/docs/Web/CSS/grid-column-gap) の各プロパティから `grid` 接頭辞が外れ、それぞれ `gap`、`row-gap`、`column-gap` となりました。従来の接頭辞付きプロパティは引き続きエイリアスとして使用できますが、将来的に廃止されます。
