---
title: "データ URL が独自オリジンとして扱われるようになりました"
date: "2018-01-24T10:37:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["57", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1324406"
      title: "Bug 1324406 - Treat 'data:' documents as unique, opaque origins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1418639"
      title: "Bug 1418639 - Page doesn't work in FF57 due to Firefox-only use of data: URIs by YUI library"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/A7LO5c6y3j4/discussion"
      title: "Intent to ship: Treating 'data:' documents as unique, opaque origins"
    - url: "https://blog.mozilla.org/security/2017/10/04/treating-data-urls-unique-origins-firefox-57/"
      title: "Mozilla Security Blog: Treating data URLs as unique origins for Firefox 57"
---
Firefox 57 以降、`data:` スキーマ接頭辞付きの [データ URL](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs) は独自の [オリジン](https://developer.mozilla.org/docs/Glossary/Origin) として扱われるようになりました。つまり、`<iframe>` に読み込まれたデータ URL 内のスクリプトは今後、それが埋め込まれたページ上のオブジェクトへアクセスできなくなります。この変更は、クロスサイトスクリプティング (XSS) 攻撃のリスクを軽減するだけでなく、Firefox を HTML 標準や他のブラウザーの挙動と一致させることを目的としたものです。

*YUI 2* のリッチテキストエディター機能が、Firefox 内でのみデータ URL を使っていることから、動作していないことが判明しています。このライブラリはもはや活発にメンテナンスされていないことから、ユーザーは有望な代替ライブラリへの移行を検討すべきでしょう。今のところ Mozilla がこの問題を Firefox 側で解決する予定はありません。
