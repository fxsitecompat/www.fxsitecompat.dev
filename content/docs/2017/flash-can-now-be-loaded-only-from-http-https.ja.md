---
title: "Flash の読み込みが HTTP/HTTPS からに制限されました"
date: "2017-03-10T16:44:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["55"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335475"
      title: "Bug 1335475 - Deny plugins from non-HTTP/HTTPS protocols"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/HdM-yCnhTYo/discussion"
      title: "Intent to implement and ship: only allow Flash on HTTP/HTTPS sites"
aliases:
    - "/ja/docs/2017/flash-will-be-loaded-only-from-https-sites/"
---
Firefox 55 以降では、`http`、`https` 以外の `file`、`ftp` といった URL プロトコルからの Flash コンテンツ読み込みが禁止されます。この変更はセキュリティ向上を目的としています。というのも、`file` プロトコルには異なる [同一オリジンポリシー](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) が適用され、またその他あまり使われていないプロトコルからの Flash コンテンツの読み込みは通常十分にテストされていないためです。

開発者は [`about:config`](https://support.mozilla.org/kb/about-config-editor-firefox) を通じて隠し設定 `plugins.http_https_only` の値を切り替えることで引き続きローカルの Flash ファイルをテストできますが、それよりもむしろ、例えば [XAMPP](https://www.apachefriends.org/) を使ってローカルウェブサーバーを立ち上げた方が良いでしょう。
