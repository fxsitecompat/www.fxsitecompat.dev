---
title: "`XMLHttpRequest.sendAsBinary()` が削除されました"
date: "2015-03-17T14:02:59-04:00"
categories: ["dom"]
tags: []
releases: ["39", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=853162"
      title: "Bug 853162 - Remove XMLHttpRequest sendAsBinary"
---
[Firefox 31 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2014/xmlhttprequest-sendasbinary-has-been-deprecated/) 非標準の [`XMLHttpRequest.prototype.sendAsBinary`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest#sendAsBinary) メソッドが削除されました。標準の `send(Blob)` メソッドで代用してください。
