---
title: "`Event.getPreventDefault()` が削除されました"
date: "2017-11-15T10:25:00-05:00"
categories: ["dom"]
tags: []
versions: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=691151"
      title: "Bug 691151 - Remove Event.prototype.getPreventDefault"
aliases:
    - "/ja/docs/2015/event-getpreventdefault-will-be-removed/"
---
[Firefox 16 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2013/obsolete-event-methods-have-been-removed/) 非標準の `Event.prototype.getPreventDefault` メソッドは、標準の [`defaultPrevented`](https://developer.mozilla.org/docs/Web/API/Event/defaultPrevented) プロパティに置き換えられる形で、Firefox 59 で削除されました。
