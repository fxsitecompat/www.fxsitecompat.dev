---
title: "2016 年 6 月より前に発行された Symantec 証明書の信頼が失われました"
date: "2018-03-12T14:12:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["60", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1434300"
      title: "Bug 1434300 - Distrust Symantec CAs affected by the distrust plan"
---
[Firefox 58 以降廃止予定](https://www.fxsitecompat.dev/ja/docs/2018/symantec-issued-certificates-will-soon-be-distrusted/) が告知されていた通り、Symantec によって 2016 年 6 月 1 日より前に発行された TLS サーバー証明書への信頼が、5 月 9 日公開の Firefox 60 で無効化されます。4 月 17 日公開の Google Chrome 66 も [同様の変更](https://developers-jp.googleblog.com/2017/09/chromes-plan-to-distrust-symantec.html) を行う予定です。GeoTrust、RapidSSL、Thawte、Verisign といったすべての Symantec ブランドが、[様々な認証局運用問題](https://wiki.mozilla.org/CA:Symantec_Issues) に起因する、この複数ベンダーによる信頼無効化措置の影響を受けます。

望まない「安全でない接続」エラーページを避けるため、Symantec から発行された証明書を使っているウェブマスターの皆さん、特に [このトップサイトリスト](https://bugzilla.mozilla.org/attachment.cgi?id=8953758) に載っているサイトの運営者は、できる限り早く [それを新しいものと交換する](https://www.symantec.com/connect/ja/blogs/symantec-ssltls) か、他の認証局から代わりの証明書を入手しなくてはなりません。私たちは、信頼できる証明書を無償で提供している [Let's Encrypt](https://letsencrypt.org/) を推奨します。

いずれも 10 月中に公開される Firefox 63 と Chrome 70 では、発行日に関わらず、すべての Symantec 証明書の信頼が取り消さます。
