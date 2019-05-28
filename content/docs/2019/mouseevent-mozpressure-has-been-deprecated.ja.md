---
title: "`MouseEvent.mozPressure` が廃止予定となりました"
date: "2019-05-28T03:35:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165211"
      title: "Bug 1165211 - Deprecate MouseEvent.mozPressure"
aliases:
    - "/ja/docs/2015/mouseevent-mozpressure-will-be-removed/"
---
`MouseEvent` インターフェイス上の `mozPressure` プロパティが廃止予定となり、近い将来削除されることとなりました。Firefox 68 は、ページ上でこのプロパティが見つかった場合、コンソールに廃止予定の警告を表示します。代わりに標準の [`PointerEvent.pressure`](https://developer.mozilla.org/docs/Web/API/PointerEvent/pressure) プロパティを使用してください。これは Firefox 59 以降使用可能となっている Pointer Events API に含まれています。
