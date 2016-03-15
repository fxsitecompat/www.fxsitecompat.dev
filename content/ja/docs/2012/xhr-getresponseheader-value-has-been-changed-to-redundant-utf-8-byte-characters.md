---
title: "`XHR.getResponseHeader()` の値が冗長な UTF-8 バイト列に変わりました"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=795867"
      title: "Bug 795867 – XHR getResponseHeader() should inflate the value"
---
[`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/DOM/XMLHttpRequest) の最新仕様に従い、[`getResponseHeader`](https://developer.mozilla.org/ja/docs/DOM/XMLHttpRequest#getResponseHeader%28%29) メソッドが冗長なエンコーディングで表現される値を返すようになりました。例えば「`…`」は「`\xE2\x80\xA6`」となります。
