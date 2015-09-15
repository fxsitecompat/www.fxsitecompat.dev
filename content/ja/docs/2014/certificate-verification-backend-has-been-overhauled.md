---
title: "証明書検証バックエンドが刷新されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["privacy-security"]
tags: []
versions: "31"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=915930": "Bug 915930 – Make mozilla::pkix the default certificate verifier"
---
mozilla::pkix と呼ばれる新しい証明書検証ライブラリが Firefox 31 で導入されました。詳しくは [Camilo Viecco のブログ記事](https://blog.mozilla.org/security/2014/04/24/exciting-updates-to-certificate-verification-in-gecko/) を参照してください。何かリグレッションに遭遇した場合は Bugzilla に [問題を報告](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Security%3A%20PSM) してください。
