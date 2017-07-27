---
title: "Cache API が不成功レスポンスを却下するようになりました"
date: "2016-02-05T15:09:00-05:00"
categories: ["dom"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244764"
      title: "Bug 1244764 - Cache .add() and .addAll() should reject if any response is not ok()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RbeEXAQ-yNQ/discussion"
      title: "mozilla.dev.platform - Heads Up: Cache API .add()/.addAll() non-backward compatible change"
---
従来、[`Cache.add`](https://developer.mozilla.org/ja/docs/Web/API/Cache/add)、[`Cache.addAll`](https://developer.mozilla.org/ja/docs/Web/API/Cache/addAll) 両メソッドは、[`fetch`](https://developer.mozilla.org/ja/docs/Web/API/Globalfetch/fetch) からの `4xx` や `5xx` エラーレスポンスを保存していました。この挙動は開発者を混乱させるものであったことから、[`Response.ok`](https://developer.mozilla.org/ja/docs/Web/API/Response/ok) プロパティが `false` となる `2xx` HTTP ステータスコード以外のレスポンスをすべて却下し、`TypeError` を投げるよう仕様が変更されました。Firefox 46 以降は更新された仕様に従っています。

副作用として、これらのメソッドは [`no-cors`](https://developer.mozilla.org/ja/docs/Web/API/Request/mode) クロスオリジンリクエストの結果として返される [`opaque`](https://developer.mozilla.org/ja/docs/Web/API/Response/type) レスポンスを常に却下するようになります。そうしたレスポンスには実際のコードの代わりに `0` ステータスコードが与えられているためです。Blink チームによれば、今のところこれはまれなケースであるとのことです。
