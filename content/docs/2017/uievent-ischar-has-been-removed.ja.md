---
title: "`UIEvent.isChar` が削除されました"
date: "2017-03-18T21:48:00-04:00"
categories: ["dom"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1347073"
      title: "Bug 1347073 - Get rid of UIEvent.isChar because no other browsers support it"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/IVcGOOeOThw/discussion"
      title: "Intent to remove UIEvent.isChar"
---
非標準の [`UIEvent.prototype.isChar`](https://developer.mozilla.org/docs/Web/API/UIEvent/isChar) プロパティが Firefox 55 で削除されました。これは macOS 以外のプラットフォームでは常に `false` を返しており、また他に対応しているブラウザーはありません。
