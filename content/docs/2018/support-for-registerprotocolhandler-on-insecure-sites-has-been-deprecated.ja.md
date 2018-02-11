---
title: "安全でないサイトでの `registerProtocolHandler()` 対応が廃止予定となりました"
date: "2018-02-11T00:01:00-05:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1429732"
      title: "Bug 1429732 - Consider making registerProtocolHandler require SecureContext"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zzBWOPMPPs0/discussion"
      title: "Intent to Unship: registerProtocolHandler() over insecure contexts"
---
現在進行中の [安全でない HTTP 廃止](https://www.fxsitecompat.com/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、Firefox 60 Nightly では、非 HTTPS サイトが [`navigator.registerProtocolHandler`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/registerProtocolHandler) メソッドを用いて、例えば `mailto` をウェブメールサービスに関連付けるなど、自サイトをプロトコルハンドラーとして登録することが許可されなくなります。この機能はあまり使われていないことから、現在の計画では Firefox 62 ですべてのチャンネルにおいてこの変更が行われます。
