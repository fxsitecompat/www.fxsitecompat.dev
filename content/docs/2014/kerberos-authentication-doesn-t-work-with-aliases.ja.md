---
title: "Kerberos 認証時にエイリアスを解決できません "
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
versions: ["35"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1108971"
      title: "Bug 1108971 – Kerberos authentication does not work with alias"
---
Firefox 35 は Kerberos 認証時にサーバーの CNAME レコード (短いドメイン名、エイリアス) を解決できないため、企業ユーザーは Kerberos プロトコルを使ったイントラネットサイトやプロキシサーバーへの認証に失敗する可能性があります。この問題は Firefox 35.0.1 で修正されました。企業ユーザーは [Firefox 31 ESR](https://www.mozilla.org/firefox/organizations/) を使えばこの問題を回避できます。
