---
title: "Flash の読み込みが HTTP(S) サイトからに制限されます"
date: "2017-02-09T05:03:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335475"
      title: "Bug 1335475 - Deny plugins from non-HTTP/HTTPS protocols"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/HdM-yCnhTYo/discussion"
      title: "Intent to implement and ship: only allow Flash on HTTP/HTTPS sites"
---
Firefox は近々、`http`、`https` 以外の `file`、`ftp`、その他 URL プロトコルからの Flash コンテンツ読み込みを制限する予定です。`file` プロトコルには異なる [同一オリジンポリシー](https://developer.mozilla.org/ja/docs/Web/Security/Same-origin_policy) が適用されること、またその他あまり使われていないプロトコルからの Flash コンテンツの読み込みは通常あまりテストされていないといった事情を踏まえ、この変更はセキュリティ向上を目的としています。変更の詳細はまだ決定されていません。
