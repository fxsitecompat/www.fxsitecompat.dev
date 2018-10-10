---
title: "Symantec、GeoTrust、RapidSSL、Thawte、Verisign 証明書への信頼が 2018 年 10 月にすべて失われます"
date: "2018-06-05T12:53:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["64"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460062"
      title: "Bug 1460062 - Enforce Symantec distrust in Firefox 63"
    - url: "https://blog.mozilla.org/security/2018/03/12/distrust-symantec-tls-certificates/"
      title: "Mozilla Security Blog: Distrust of Symantec TLS Certificates"
    - url: "https://blog.mozilla.org/security/2018/07/30/update-on-the-distrust-of-symantec-tls-certificates/"
      title: "Update on the Distrust of Symantec TLS Certificates"
---
[様々な認証局運用問題](https://wiki.mozilla.org/CA:Symantec_Issues) に起因する、複数ベンダーによる Symantec に対する信頼無効化措置の最終段階として、10 月 23 日公開の Firefox 63 は、Symantec から発行されたすべての既存 TLS サーバー証明書への信頼を取り消します。これには、GeoTrust、RapidSSL、Thawte、Verisign ブランド傘下で発行されたものも含まれます。10 月 16 日公開の [Google Chrome 70](https://developers-jp.googleblog.com/2018/04/distrust-of-symantec-pki-immediate.html) でも同様の変更が行われます。

[Firefox 58](https://www.fxsitecompat.com/ja/docs/2018/symantec-issued-certificates-will-soon-be-distrusted/) 以降、影響を受ける証明書に対してコンソール警告が表示されており、[Firefox 60](https://www.fxsitecompat.com/ja/docs/2018/symantec-certificates-issued-before-june-2016-are-now-distrusted/) では 2016 年 6 月より前に発行された証明書への信頼が既に失われています。Firefox 63 以降、発行日に関わらず、Symantec から発行された証明書を使ったサイトに対して「安全でない接続」のエラーページが表示されます。

望まないエラーページを避けるため、それらのいずれかの証明書を使っているウェブマスターの皆さんは、できる限り早く [それを新しいものと交換する](https://www.symantec.com/connect/ja/blogs/symantec-ssltls) か、他の認証局から代わりの証明書を入手しなくてはなりません。私たちは、信頼できる証明書を無償で提供している [Let's Encrypt](https://letsencrypt.org/) を推奨します。

**更新**: この変更は 8 月 14 日に [Firefox Nightly](https://blog.nightly.mozilla.org/2018/08/14/symantec-distrust-in-firefox-nightly-63/) 上で行われ、影響を受けるサイトは [Bug 1484006](https://bugzilla.mozilla.org/show_bug.cgi?id=1484006) で把握されています。Firefox Beta および Developer Edition は 9 月 25 日にこの変更を伴って更新されます。

**更新 2**: 影響を受けるサイトがまだ多数存在することから、9 月 25 日公開の Firefox 63 Beta 9 はまだ初期設定で信頼取り消しを有効化していません。Mozilla のエンジニアは、いつ有効化すべきか決定するため、状況を注意深く見守っています。

**更新 3**: Mozilla は 10 月中旬公開の Firefox 64 Beta へ [信頼取り消しを延期する](https://blog.mozilla.org/security/2018/10/10/delaying-further-symantec-tls-certificate-distrust/) ことを正式に発表しました。
