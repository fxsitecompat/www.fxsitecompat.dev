---
title: "Symantec から発行された証明書の信頼が近く失われます"
date: "2018-03-02T21:48:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["58"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1409259"
      title: "Bug 1409259 - Implement a console warning for Symantec CAs affected by the distrust plan"
---
Mozilla は、他の複数のブラウザーベンダーとともに、Symantec によって発行されたすべての TLS サーバー証明書への信頼を無効化する決定を下しました。これは、[広範な調査](https://wiki.mozilla.org/CA:Symantec_Issues) と議論を通じて発見された不適切な認証局運営に起因するものです。Firefox の [今後の信頼無効化措置](https://wiki.mozilla.org/CA/Upcoming_Distrust_Actions) は [Google Chrome](https://developers-jp.googleblog.com/2017/09/chromes-plan-to-distrust-symantec.html) と歩調を合わせており、GeoTrust、RapidSSL、Thawte、Verisign といったすべての Symantec ブランドに適用されます。

* 2018 年 5 月 9 日公開の Firefox 60 では、2016 年 6 月より前に発行された Symantec 証明書を使ったサイトに対して「安全でない接続」のエラーページが表示されます
* 2018 年 10 月 16 日公開の Firefox 63 では、Symantec のすべてのルート証明書が削除され、発行日に関わらず、Symantec 証明書を使ったサイトに対して「安全でない接続」のエラーページが表示されます

これらの期日より前に、Symantec から発行された証明書を使っているウェブマスターの皆さんは、[それを新しいものと交換する](https://www.symantec.com/connect/ja/blogs/symantec-ssltls) か、[Let's Encrypt](https://letsencrypt.org/) など他の認証局から代わりの証明書を入手しなくてはなりません。Firefox 58 と 59 では、Symantec 証明書を使ったサイトに対してコンソール警告を表示し、移行を促します。
