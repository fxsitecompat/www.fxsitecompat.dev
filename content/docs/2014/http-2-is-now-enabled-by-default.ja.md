---
title: "HTTP/2 が初期設定で有効となりました"
date: "2014-09-01T22:12:15-04:00"
categories: ["networking"]
tags: []
versions: ["34"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1047594"
      title: "Bug 1047594 – Enable http/2 (and alpn) by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1027720"
      title: "Bug 1027720 – Restrict HTTP/2 connections to AEAD ciphers only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1077806"
      title: "Bug 1077806 – tweetdeck.twitter.com and twitter.com history doesn\'t load in Nightly 35.0a1 and Aurora 34.0a2 when http2 enabled"
---
[HTTP/2](http://http2.github.io/) 仕様のドラフト 14 が実装され、AEAD 暗号化スイートを使用した接続について初期設定で有効となりました。もし何かリグレッションに遭遇した場合は、Bugzilla へ [問題を報告してください](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Networking%3A%20HTTP)。
