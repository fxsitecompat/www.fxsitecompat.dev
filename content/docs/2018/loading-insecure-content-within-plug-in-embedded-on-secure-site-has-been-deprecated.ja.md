---
title: "安全なサイトに埋め込まれたプラグイン内部での安全でないコンテンツの読み込みが廃止予定となりました"
date: "2018-03-09T12:04:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1441794"
      title: "Bug 1441794 - Add deprecation warning to OBJECT_SUBREQUEST for stable releases"
---
[混在コンテンツ](https://developer.mozilla.org/ja/docs/Web/Security/Mixed_content) ブロックの強化を目的として、Firefox は近く、安全な HTTPS サイト上に埋め込まれたプラグインが安全でない非 HTTPS サイトから配信されたコンテンツの読み込みを禁止します。Firefox 60 以降、こうしたケースについてコンソールに警告が表示されます。

Adobe Flash が Firefox で現在対応されている唯一のプラグインであり、そのためこの変更は特に外部 XML データの読み込みに影響します。解決策は、データも同じく安全なサイトから配信することです。
