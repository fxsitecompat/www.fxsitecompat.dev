---
title: "WebSockets の接続切断処理が最新仕様に合わせて更新されました"
date: "2012-10-09T06:00:00-04:00"
categories: ["networking"]
tags: []
versions: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=695636"
      title: "Bug 695636 - Update close steps to adhere to WS spec."
---
コード内で `close` メソッドが呼び出された際の切断処理中に `error` や `close` イベントが発生しないようにするなど、最新の仕様に合わせて [WebSockets](https://developer.mozilla.org/docs/Web/API/WebSockets_API) 実装が更新されました。
