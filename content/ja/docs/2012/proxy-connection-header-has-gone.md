---
title: "`Proxy-Connection` ヘッダが廃止されました"
date: "2012-12-03T03:53:26-05:00"
categories: ["networking"]
tags: []
versions: ["18"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=570283": "Bug 570283 – Stop sending Proxy-Connection"
---
HTTP プロキシ設定時に送信されていた `Proxy-Connection` リクエストヘッダが廃止されました。このヘッダは非標準で、実際にはうまく機能していませんでした。
