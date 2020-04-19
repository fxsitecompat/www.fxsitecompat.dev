---
title: "`Node.isSupported()` が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=849661"
      title: "Bug 849661 – Remove support for Node.hasAttributes()"
---
[`Node.isSupported`](https://developer.mozilla.org/docs/Web/API/Node.isSupported) メソッドは、仕様から削除されたため、使用できなくなりました。[Firefox 19](https://www.fxsitecompat.dev/ja/docs/2012/hasfeature-issupported-methods-now-always-return-true/) 以降、このメソッドは常に `true` を返していました。
