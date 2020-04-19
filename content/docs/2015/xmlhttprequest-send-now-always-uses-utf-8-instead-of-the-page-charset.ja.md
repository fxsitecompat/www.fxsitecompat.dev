---
title: "`XMLHttpRequest.send()` がページの文字コードではなく常に UTF-8 を使うようになりました"
date: "2015-01-16T09:37:54-05:00"
categories: ["dom"]
tags: []
releases: ["37", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1109486"
      title: "Bug 1109486 – XMLHttpRequest.send(document) should unconditionally encode as UTF-8"
---
[`XMLHttpRequest.send`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest#send%28%29) メソッドの実装が更新され、仕様に従って、ドキュメントの文字エンコーディングではなく常に `UTF-8` で渡されたデータを送信するようになりました。
