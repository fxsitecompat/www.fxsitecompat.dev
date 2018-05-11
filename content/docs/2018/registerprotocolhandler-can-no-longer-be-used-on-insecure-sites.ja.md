---
title: "`registerProtocolHandler()` が安全でないサイトでは使用できなくなりました"
date: "2018-05-11T14:47:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460506"
      title: "Bug 1460506 - registerProtocolHandler require SecureContext in stable"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zzBWOPMPPs0/discussion"
      title: "Intent to Unship: registerProtocolHandler() over insecure contexts"
---
Firefox 62 以降、安全でないアプリケーションがプロトコルハンドラーとしてブラウザーへ登録されるのを防ぐため、非 HTTPS サイト上では [`navigator.registerProtocolHandler`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/registerProtocolHandler) メソッドが `undefined` となります。このセキュリティ制限は [バージョン 60](https://www.fxsitecompat.com/ja/docs/2018/support-for-registerprotocolhandler-on-insecure-sites-has-been-deprecated/) 以降の Firefox Nightly と早期 Beta/DevEdition には既に導入されています。
