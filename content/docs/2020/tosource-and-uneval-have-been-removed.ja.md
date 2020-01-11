---
title: "`toSource()` と `uneval()` が廃止されました"
date: "2020-01-11T01:37:00-05:00"
categories: ["javascript"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1565170"
      title: "Bug 1565170 - Disable toSource/uneval in non-chrome code"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/WVk3jvpzsgs/discussion"
      title: "Intent to unship: JavaScript toSource and uneval"
---
Firefox 74 で、`Array`、`Date`、`Function` といった `Object` に由来するすべてのオブジェクトに継承されていた非標準の [`Object.prototype.toSource`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/toSource) メソッドが、[`uneval`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/uneval) グローバル関数とともに削除されました。標準の `toString` メソッドや `eval` グローバル関数と異なり、他のどのブラウザーもこれらの Netscape の遺産に対応していないため、互換性リスクは低いはずです。
