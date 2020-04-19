---
title: "サードパーティ Cookie は初期設定でブロックされます"
date: "2013-02-24T03:44:31-05:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["22"]
statuses: "postponed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818340"
      title: "Bug 818340 – Block cookies from sites I haven\'t visited"
---
Firefox 22 以降、ユーザーがオンラインプライバシーをより柔軟に管理できるよう、Apple Safari のように、サードパーティ Cookie が初期設定でブロックされるようになります。詳しくは [Mozilla Privacy Blog の投稿](https://blog.mozilla.org/privacy/2013/02/25/firefox-getting-smarter-about-third-party-cookies/) と Jonathan Mayer の [Firefox の新 Cookie ポリシーに関する FAQ](http://webpolicy.org/2013/02/22/the-new-firefox-cookie-policy/) をご覧ください。

<ins>更新: サードパーティ Cookie をブロックした場合の影響についてデータを収集・解析するため、[**この変更は延期されました**](https://bugzilla.mozilla.org/show_bug.cgi?id=851606)。Beta および Release チャンネルでは、初期設定は変更されず、サードパーティ Cookie は許可されます。詳しい経緯は [Brendan Eich のブログ記事](https://brendaneich.com/2013/05/c-is-for-cookie/) を参照してください。</ins>

**更新 2**: [Firefox 65](https://www.fxsitecompat.dev/ja/docs/2018/third-party-tracking-cookies-are-now-blocked-by-default/) 以降、サードパーティトラッキング Cookie は初期設定でブロックされます。
