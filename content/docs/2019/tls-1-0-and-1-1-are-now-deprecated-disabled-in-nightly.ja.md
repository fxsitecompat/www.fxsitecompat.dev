---
title: "TLS 1.0 と 1.1 が廃止予定となり、Nightly では無効化されました"
date: "2019-09-27T22:53:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1579270"
      title: "Bug 1579270 - Disable TLS 1.0 and 1.1 for Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1606733"
      title: "Bug 1606733 - Disable TLS 1.0 and 1.1 in Beta"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8EFRYDR3N1c/discussion"
      title: "Intent to unship: TLS 1.0 and TLS 1.1"
    - url: "https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/"
      title: "TLS 1.0 and 1.1 Removal Update - Mozilla Hacks"
aliases:
    - "/ja/docs/2019/tls-1-0-and-1-1-are-now-deprecated/"
---
[Transport Layer Security](https://developer.mozilla.org/docs/Web/Security/Transport_Layer_Security) (TLS) 1.0 と 1.1 への対応は廃止予定となり、2020 年 3 月にはすべての主要ブラウザーから削除されます。廃止に備えて Firefox Nightly ではそれらの TLS 旧バージョンが初期設定で無効化され、これによりブラウザーは [安全な接続ができませんでした](https://support.mozilla.org/kb/secure-connection-failed-firefox-did-not-connect) というエラーページを表示して、TLS 1.2 や 1.3 を使用していないウェブサーバーへのアクセスをブロックします。

今後もあなたのサーバーが安全でアクセス可能となるよう、TLS の新バージョンが有効になっていることを確かめましょう。詳しくは [この Mozilla Hacks ブロク記事](https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/) を参照してください。

**更新**: Firefox 73 以降、TLS 1.0 と 1.1 は Beta チャンネルでも無効化されています。

**更新 2**: [Firefox 74](https://www.fxsitecompat.dev/ja/docs/2020/tls-1-0-1-1-support-has-been-removed/) ですべてのチャンネルから対応が削除されました。
