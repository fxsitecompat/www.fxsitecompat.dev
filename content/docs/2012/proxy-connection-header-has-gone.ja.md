---
title: "`Proxy-Connection` ヘッダーが廃止されました"
date: "2012-12-03T03:53:26-05:00"
categories: ["networking"]
tags: []
versions: ["18"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=570283"
      title: "Bug 570283 – Stop sending Proxy-Connection"
---
HTTP プロキシ設定時に送信されていた `Proxy-Connection` リクエストヘッダーが廃止されました。このヘッダーは非標準で、実際にはうまく機能していませんでした。
