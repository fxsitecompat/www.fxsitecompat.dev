---
title: "インタラクティブな SVG 内の一部要素が特定の状況で見えなくなります"
date: "2016-03-24T17:36:00-04:00"
categories: ["svg"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1258650"
      title: "Bug 1258650 - Yahoo finance chart comparison \"overlays\" not displayed properly"
---
複雑でインタラクティブな SVG 内部の一部要素が特定の状況下で見えなくなり、それらの要素を表示するために本来不要なユーザインタラクションが求められるというリグレッションが Firefox 45 で発生しました。このバグは *Yahoo! Finance* の株価チャートに影響しています。Mozilla 開発者が解決策に取り組みます。
