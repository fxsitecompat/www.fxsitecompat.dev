---
title: "`focus`、`blur` 両イベントが `FocusEvent` になりました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
releases: ["24", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=855741"
      title: "Bug 855741 – FocusEvent interface is missing"
---
[`focus`](https://developer.mozilla.org/docs/Web/Reference/Events/focus) イベントと [`blur`](https://developer.mozilla.org/docs/Web/Reference/Events/blur) イベントが更新され、[`Event`](https://developer.mozilla.org/docs/Web/API/Event) インターフェイスの代わりに [`FocusEvent`](https://developer.mozilla.org/docs/Web/API/FocusEvent) インターフェイスのインスタンスとなりました。これにより DOM Level 3 Events 仕様に準拠した実装となります。
