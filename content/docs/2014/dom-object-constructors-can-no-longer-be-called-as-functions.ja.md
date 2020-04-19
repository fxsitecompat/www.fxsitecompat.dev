---
title: "DOM オブジェクトコンストラクターを関数として呼び出せなくなりました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
releases: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=916644"
      title: "Bug 916644 – Disallow calling WebIDL constructors as functions on the web"
---
従来、[WebIDL](https://dxr.mozilla.org/mozilla-central/source/dom/webidl/) コンストラクターは [`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) 演算子なしに呼び出すことが可能でした。Firefox 30 以降、そうしたコードは Chrome や Safari のように [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) を投げるようになります。例えば `var req = XMLHttpRequest();` は `var req = new XMLHttpRequest();` とすべきです。
