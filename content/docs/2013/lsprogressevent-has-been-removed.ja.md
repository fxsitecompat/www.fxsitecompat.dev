---
title: "`LSProgressEvent` が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=845631"
      title: "Bug 845631 – Remove nsXMLHttpProgressEvent"
---
主に [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) とともに使用され、Firefox 10 以降 [非推奨](https://bugzilla.mozilla.org/show_bug.cgi?id=616672) となっていた古いインターフェイス [`LSProgressEvent`](https://www.w3.org/TR/DOM-Level-3-LS/load-save.html#LS-LSProgressEvent) が、`input`、`position`、`totalSize` 属性とともに削除されました。[Monitoring progress](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest#Monitoring_progress) の項で説明されている通り、`loaded` および `total` 属性を含む一般的な [`ProgressEvent`](https://developer.mozilla.org/docs/Web/API/ProgressEvent) インターフェイスで代用してください。
