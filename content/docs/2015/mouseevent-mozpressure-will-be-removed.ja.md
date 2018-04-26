---
title: "`MouseEvent.mozPressure` が削除されます"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165211"
      title: "Bug 1165211 - Remove MouseEvent.mozPressure."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=822898"
      title: "Bug 822898 - Implement pointer events"
---
`MouseEvent.mozPressure` プロパティは標準の `PointerEvent.pressure` プロパティに置き換えられる形で削除されます。[Pointer Events API](https://www.w3.org/TR/pointerevents/) は現在実装が進められています。
