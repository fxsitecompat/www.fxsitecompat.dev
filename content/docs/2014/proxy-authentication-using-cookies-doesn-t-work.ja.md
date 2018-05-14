---
title: "Cookie を使ったプロキシ認証が機能しません "
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
versions: ["35"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1121895"
      title: "Bug 1121895 – Proxy authentication with Auth-Cookies not working anymore"
---
Firefox 35 では 407 Proxy Authentication HTTP レスポンスを使った Cookie 注入を許してしまう [セキュリティバグ](http://www.mozilla-japan.org/security/announce/2015/mfsa2015-04.html) が修正されました。その副作用として、企業内イントラネットサイトのための正規 Cookie 認証も、プロキシサーバーによって認証用 Cookie がセットできなくなったために機能しなくなっています。Mozilla 開発者はこの問題をどう安全に解決すべきか議論を進めています。企業ユーザーは [Firefox 31 ESR](https://www.mozilla.org/firefox/organizations/) を使えばこの問題を回避できます。
