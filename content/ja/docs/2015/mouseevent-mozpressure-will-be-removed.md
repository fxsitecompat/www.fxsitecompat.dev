---
title: "`MouseEvent.mozPressure` が削除されます"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1165211": "Bug 1165211 - Remove MouseEvent.mozPressure."
    "https://bugzilla.mozilla.org/show_bug.cgi?id=822898": "Bug 822898 - Implement pointer events"
---
`MouseEvent.mozPressure` プロパティは標準の `PointerEvent.pressure` プロパティに置き換えられる形で削除されます。[Pointer Events API](http://www.w3.org/TR/pointerevents/) は現在実装が進められています。
