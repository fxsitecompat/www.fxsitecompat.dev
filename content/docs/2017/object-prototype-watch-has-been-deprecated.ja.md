---
title: "`Object.prototype.watch` が廃止予定となりました"
date: "2017-08-21T16:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=638054"
      title: "Bug 638054 - JavaScript Object.prototype.watch should be removed, once an adequate debugger-only replacement exists"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934669"
      title: "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
aliases:
    - "/ja/docs/2015/object-prototype-watch-will-be-removed/"
    - "/ja/docs/2017/object-prototype-watch-will-be-removed/"
---
非標準の [`Object.prototype.watch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/watch)、[`unwatch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) メソッドは廃止予定となり、近い将来削除されることとなりました。Firefox 57 以降、コンソールにこれらのメソッドに対する警告が表示されます。標準の [`Proxy`] (https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Proxy) あるいは [`Reflect`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Reflect) オブジェクトを代わりに使用してください。
