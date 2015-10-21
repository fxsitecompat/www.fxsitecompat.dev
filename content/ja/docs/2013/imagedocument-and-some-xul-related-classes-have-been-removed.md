---
title: "`ImageDocument` と一部の XUL 関連クラスが削除されました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=885177": "Bug 885177 – Make window.ImageDocument ChromeOnly"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=898687": "Bug 898687 – Remove XULTreeBuilder from content"
---
非標準の `ImageDocument` インタフェースと、`BoxObject`、`TreeColumn`、`TreeColumns`、`TreeContentView`、`TreeSelection`、`XULControllers`、`XULTemplateBuilder`、`XULTreeBuilder` インタフェースが、Web コンテンツから使用できなくなりました。
