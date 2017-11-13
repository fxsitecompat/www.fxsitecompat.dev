---
title: "`Event.getPreventDefault` が削除されます"
date: "2015-10-27T22:54:00-07:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=691151"
      title: "Bug 691151 - Remove Event.prototype.getPreventDefault"
---
[Firefox 16 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2013/obsolete-event-methods-have-been-removed/) 非標準の `Event.prototype.getPreventDefault` メソッドは、標準の [`Event.prototype.defaultPrevented`](https://developer.mozilla.org/ja/docs/Web/API/Event/defaultPrevented) プロパティに置き換えられる形で将来的に削除されます。
