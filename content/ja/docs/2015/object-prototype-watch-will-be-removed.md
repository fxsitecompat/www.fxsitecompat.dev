---
title: "`Object.prototype.watch` が削除されます"
date: "2015-10-26T15:35:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=638054": "Bug 638054 - JavaScript Object.prototype.watch should be removed, once an adequate debugger-only replacement exists"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=934669": "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=800355": "Bug 800355 - Implement Object.observe"
---
非標準の [`Object.prototype.watch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/watch)、[`Object.prototype.unwatch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) メソッドは将来的に削除されます。標準の [`Proxy`] (https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Proxy) オブジェクトを代わりに使用してください。
