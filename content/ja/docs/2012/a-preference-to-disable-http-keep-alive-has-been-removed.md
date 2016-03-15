---
title: "HTTP Keep-Alive を無効化する設定が削除されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=770331"
      title: "Bug 770331 – Remove HTTP Keep-Alive disable pref"
---
Firefox では HTTP Keep-Alive (持続的接続) が有効になっており、何らかの不具合が生じた場合は隠し設定 `network.http.keep-alive` で無効化することが可能となっています。Firefox 17 ではこの設定が廃止され、Keep-Alive が常時有効となります。
