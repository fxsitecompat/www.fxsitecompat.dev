---
title: "CSS クラスが異なる要素に適用されてしまいます"
date: "2015-11-07T00:03:00-08:00"
categories: ["css"]
tags: []
versions: ["42"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222226"
      title: "Bug 1222226 - CSS class applied to wrong elements"
---
特定のタイミングで、例えば [`Element.className`](https://developer.mozilla.org/docs/Web/API/Element/className) によって動的に追加された CSS クラスが異なる要素に適用され、予期せぬページのスタイリングにつながるリグレッションが Firefox 42 で発生しました。Mozilla 開発者が解決策に取り組んでいます。

**更新**: この問題は Firefox 43 で修正されました。
