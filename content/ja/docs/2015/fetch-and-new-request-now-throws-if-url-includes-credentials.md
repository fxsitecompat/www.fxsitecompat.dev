---
title: "`fetch()` と `new Request()` が URL に認証情報が含まれる場合に例外を投げるようになりました"
date: "2015-09-24T01:15:00-05:00"
categories: ["dom"]
tags: []
versions: "43"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1195820": "Bug 1195820 - fetch() and new Request() should throw TypeError on URL with username/password"
---
Firefox に実装されている [`fetch`](https://developer.mozilla.org/ja/docs/Web/API/GlobalFetch/fetch) メソッドと [`Request`](https://developer.mozilla.org/ja/docs/Web/API/Request/Request) コンストラクタが、`http://user:password@example.com` のようなユーザ名やパスワードを含む URL を誤って受け入れていました。Firefox 43 およびそれ以降のバージョンでは、Fetch API 仕様に従って、そうした場合には `TypeError` が投げられます。
