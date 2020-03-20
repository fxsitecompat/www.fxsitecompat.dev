---
title: "TLS 1.0/1.1 対応が廃止されました"
date: "2020-01-08T19:23:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["74"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1606734"
      title: "Bug 1606734 - Disable TLS 1.0 and 1.1 by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623534"
      title: "Bug 1623534 - Remote pref override to re-enable TLS 1.0"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623536"
      title: "Bug 1623536 - Re-enable TLS 1.0 in Firefox 75 (Beta)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8EFRYDR3N1c/discussion"
      title: "Intent to unship: TLS 1.0 and TLS 1.1"
    - url: "https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/"
      title: "TLS 1.0 and 1.1 Removal Update - Mozilla Hacks"
---
[Firefox 71](https://www.fxsitecompat.dev/ja/docs/2019/tls-1-0-and-1-1-are-now-deprecated-disabled-in-nightly/) 以降廃止予定となっていた [Transport Layer Security](https://developer.mozilla.org/docs/Web/Security/Transport_Layer_Security) (TLS) プロトコルのバージョン 1.0 と 1.1 への対応が Firefox 74 ですべてのチャンネルから削除されました。すべてのメジャーブラウザーが 2020 年初めに TLS 旧バージョンへの対応を打ち切る予定となっています。

あなたのウェブサーバー上で必ず TLS 1.2 か 1.3 を有効にしましょう。さもないと Firefox は [安全な接続ができませんでした](https://support.mozilla.org/kb/secure-connection-failed-firefox-did-not-connect) というエラーページを表示して、その新バージョンを使用していないサーバーへユーザーがアクセスするのをブロックします。詳しくは [この Mozilla Hacks ブロク記事](https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/) を参照してください。

**更新**: Mozilla は Firefox 74 と 75 Beta の TLS 1.0/1.1 対応を一時的に再有効化する方針です。設定変更は、既に公開されている Firefox 74 に対してはリモートで適用されます。これは、新型コロナウイルス (COVID-19) の流行を受けて、現在多くの人が在宅勤務を強いられオンラインツールに依存していますが、一部の重要な政府機関サイトがまだ TLS 1.2 に対応していないためです。また COVID-19 を理由として、Google が [TLS 1.0/1.1 対応を廃止](https://www.chromestatus.com/feature/5759116003770368) する予定となっていた [Chrome 81 の公開を延期](https://blog.chromium.org/2020/03/upcoming-chrome-releases.html) しています。状況が変わり次第このドキュメントを更新します。
