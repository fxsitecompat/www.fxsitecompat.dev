---
title: "RC4 対応が完全に削除されました"
date: "2016-11-17T20:01:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["50"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268728"
      title: "Bug 1268728 - Remove ability to enable RC4"
---
RC4 対応は [Firefox 36](https://www.fxsitecompat.dev/ja/docs/2014/rc4-support-has-been-deprecated/) 以降廃止予定となり、[Firefox 44](https://www.fxsitecompat.dev/ja/docs/2015/rc4-is-now-completely-disabled-by-default/) 以降初期設定で無効化されています。ただし、一部のイントラネットアプリケーションが未更新の場合などは、一時的な回避策として、隠し設定を通じて引き続き有効化することは可能でした。

1 年間の猶予期間を過ぎ、Firefox 50 でこの設定の上書きが不可能になったことに伴い、RC4 対応は完全に廃止されました。これは同様のセキュリティ対策を講じた 8 月公開の Google Chrome 53 に続くものです。今後 Firefox は、RC4 暗号を使用しているサイトに遭遇した場合、単に `SSL_ERROR_NO_CYPHER_OVERLAP` エラーを表示するだけとなります。
