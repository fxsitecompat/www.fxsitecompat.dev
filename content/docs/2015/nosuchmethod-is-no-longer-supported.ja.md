---
title: "`__noSuchMethod__` 対応が打ち切られました"
date: "2015-09-22T09:37:00-04:00"
categories: ["javascript"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=683218"
      title: "Bug 683218 - can we remove __noSuchMethod__, use proxies instead?"
---
[Firefox 39 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2015/nosuchmethod-has-been-deprecated/) 非標準プロパティ [`Object.prototype.__noSuchMethod__`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/noSuchMethod) への対応が Firefox 44 で削除されました。そうしたキャッチオール機構を実装したい場合は、ECMAScript 2015 (ES6) の [`Proxy`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) オブジェクトで代用可能です。
