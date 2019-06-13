---
title: "ウェブコンソールが SSLv3 や RC4 を使用したサイトで警告を表示するようになりました"
date: "2015-01-16T09:37:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["37"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1092835"
      title: "Bug 1092835 – Log usage of weak ciphers in the console"
---
[ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) が、安全でなく廃止予定となっている SSL 3.0 プロトコルや RC4 暗号スイートを使ったサイト上で警告を表示するようになりました。ウェブマスターの皆さんには、サーバーを更新してより強力な暗号化を提供するよう強く推奨します。

**更新**: SSLv3 対応は [Firefox 39 で削除されました](https://www.fxsitecompat.dev/ja/docs/2015/sslv3-support-has-been-removed/)。
