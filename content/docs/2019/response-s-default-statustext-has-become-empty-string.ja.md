---
title: "`Response` の既定 `statusText` が空文字列となりました"
date: "2019-05-13T04:32:00-04:00"
categories: ["dom", "networking"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1508996"
      title: "Bug 1508996 - Change Response's statusText's default"
---
Firefox 67 以降、[`Response.statusText`](https://developer.mozilla.org/docs/Web/API/Response/statusText) プロパティの初期値が空文字列となりました。これは今まで `"OK"` でした。単純にリクエストが成功したかどうかを確認したい場合は、代わりに真偽値の [`ok`](https://developer.mozilla.org/docs/Web/API/Response/ok) プロパティを使った方が良いでしょう。
