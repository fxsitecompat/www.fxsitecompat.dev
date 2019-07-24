---
title: "`URL.createObjectURL()` は Service Worker 内で使用できなくなりました"
date: "2018-08-14T13:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1264182"
      title: "Bug 1264182 - remove URL.createObjectURL from ServiceWorker"
---
静的メソッドの `URL.createObjectURL` と `URL.revokeObjectURL` は、`blob` URL のライフサイクル問題を生じさせることから、最新の Service Workers 仕様に従い Service Worker コンテキストから隠されるようになりました。これらは、専用 Worker や共有 Worker 内、ならびに `window` 上では引き続き使用可能です。
