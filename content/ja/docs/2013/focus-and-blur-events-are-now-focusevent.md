---
title: "`focus`、`blur` 両イベントが `FocusEvent` になりました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: ["24"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=855741": "Bug 855741 – FocusEvent interface is missing"
---
[`focus`](https://developer.mozilla.org/ja/docs/Web/Reference/Events/focus) イベントと [`blur`](https://developer.mozilla.org/ja/docs/Web/Reference/Events/blur) イベントが更新され、[`Event`](https://developer.mozilla.org/ja/docs/Web/API/Event) インタフェースの代わりに [`FocusEvent`](https://developer.mozilla.org/ja/docs/Web/API/FocusEvent) インタフェースのインスタンスとなりました。これにより DOM Level 3 Events 仕様に準拠した実装となります。
