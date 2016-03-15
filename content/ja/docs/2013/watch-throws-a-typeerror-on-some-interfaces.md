---
title: "一部のインタフェース上で `watch()` が `TypeError` を投げます"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
versions: ["23"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=903332"
      title: "Bug 903332 – document.watch() results in \"TypeError: can\'t watch non-native objects of class Proxy\""
---
Firefox 23 以降、オブジェクトプロパティへ行われた変更の監視に使用できる非標準の [`watch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) メソッドが、[`Document`](https://developer.mozilla.org/ja/docs/Web/API/Document)、[`HTMLSelectElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLSelectElement)、あるいはおそらくその他いくつかの DOM 要素インタフェースを対象とした場合に [`TypeError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げます。回避策は [`Proxy`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Proxy) を使うことです。なお、`watch` と [`unwatch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) は将来的に削除される可能性があり、それら Firefox 固有メソッドの使用は避けるべきです。このリグレッションは Firefox 27 で修正されました。
