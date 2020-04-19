---
title: "`image-rendering:crisp-edges` の接頭辞が外れました"
date: "2018-10-31T23:50:00-04:00"
categories: ["css"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496617"
      title: "Bug 1496617 - Unprefix `image-rendering: crisp-edges`"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503753"
      title: "Bug 1503753 - remove image-rendering:-moz-crisp-edges"
---
[`image-rendering`](https://developer.mozilla.org/docs/Web/CSS/image-rendering) CSS プロパティ用の `crisp-edges` 値の接頭辞が Firefox 65 で外れました。`-moz-crisp-edges` への対応は将来的に廃止されます。
