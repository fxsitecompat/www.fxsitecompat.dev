---
title: "`XMLHttpRequest` が HTML ドキュメントを `application/xml` ではなく `text/html` として送信するようになりました"
date: "2015-10-23T02:04:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=918771"
      title: "Bug 918771 - XMLHttpRequest (XHR) send() of an HTML document sends it as application/xml, not text/html"
---
これまで、Firefox の [`XMLHttpRequest.send`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest#send%28%29) メソッドは HTML ドキュメントを `application/xml` MIME タイプとして送信し、XML 宣言 `<?xml version="1.0"?>` をそのドキュメントに付加していました。相互運用性を高めるため、XMLHttpRequest 仕様と Firefox の実装が更新され、HTML ドキュメントは UTF-8 文字エンコーディングの `text/html` として送信されるようになりました。
