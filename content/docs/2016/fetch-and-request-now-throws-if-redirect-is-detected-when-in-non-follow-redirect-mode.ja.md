---
title: "`follow` 以外のリダイレクトモード時にリダイレクトが検出された場合、`fetch` と `Request` は例外を投げます"
date: "2016-05-10T20:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1243792"
      title: "Bug 1243792 - add fetch Response.redirected and additional security restrictions"
---
オープンリダイレクタのリスクを防ぐため、リクエストの `redirect` オプションが `manual` あるいは `error` に設定され、そのレスポンスに 1 つあるいは複数のリダイレクトが含まれていた場合、[`fetch`](https://developer.mozilla.org/docs/Web/API/GlobalFetch/fetch) メソッドと [`Request`](https://developer.mozilla.org/docs/Web/API/Request/Request) コンストラクターはネットワークエラーを投げるようになりました。また、[`Response`](https://developer.mozilla.org/docs/Web/API/Response) インターフェイスに `redirected` プロパティが追加されたことで、開発者はこの新しいプロパティをチェックして信頼できないレスポンスを防ぐことが可能となりました。
