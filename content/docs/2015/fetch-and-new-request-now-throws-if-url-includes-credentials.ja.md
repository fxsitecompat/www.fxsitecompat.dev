---
title: "`fetch()` と `new Request()` が URL に認証情報が含まれる場合に例外を投げるようになりました"
date: "2015-09-24T01:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1195820"
      title: "Bug 1195820 - fetch() and new Request() should throw TypeError on URL with username/password"
---
Firefox に実装されている [`fetch`](https://developer.mozilla.org/docs/Web/API/GlobalFetch/fetch) メソッドと [`Request`](https://developer.mozilla.org/docs/Web/API/Request/Request) コンストラクターが、`http://user:password@example.com` のようなユーザー名やパスワードを含む URL を誤って受け入れていました。Firefox 43 およびそれ以降のバージョンでは、Fetch API 仕様に従って、そうした場合には `TypeError` が投げられます。
