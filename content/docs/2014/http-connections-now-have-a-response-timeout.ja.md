---
title: "HTTP 接続にレスポンスタイムアウトが設定されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["networking"]
tags: []
versions: ["29", "31-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=947391"
      title: "Bug 947391 – HTTP connections (exc. XHR, SPDY) should have a response timeout"
---
Firefox は、XMLHttpRequest と SPDY セッションを除いて、レスポンスに時間が掛かりすぎる場合に HTTP 接続を中止するタイムアウトを有効化しました。初期値は 300 秒、つまり 5 分となっています。あなたのアプリケーションで巨大なデータを処理していて、この変更による影響を受ける場合、[about:config](http://kb.mozillazine.org/About:config) を通じて `network.http.response.timeout` 設定値をより大きな数字に変更できます。
