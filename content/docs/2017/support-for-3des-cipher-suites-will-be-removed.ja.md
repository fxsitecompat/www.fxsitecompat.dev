---
title: "3DES 暗号スイート対応が削除されます"
date: "2017-09-20T20:40:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1227524"
      title: "Bug 1227524 - Establish deprecation date for 3DES"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1386754"
      title: "Bug 1386754 - Disable 3DES in TLS Handshake for Nightly builds"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1386908"
      title: "Bug 1386908 - Disable 3DES in TLS Handshake for early beta builds"
---
Firefox は TLS ハンドシェイクにおける [トリプル DES](https://en.wikipedia.org/wiki/Triple_DES) (3DES) 暗号スイートを廃止予定としており、近い将来対応を削除する予定です。バージョン 57 以降の Firefox Nightly チャンネルでは既に無効化されており、影響を受けるサイトへアクセスすると `SSL_ERROR_NO_CYPHER_OVERLAP` エラーが表示されます。

次のステップは Developer Edition を含む早期 Beta チャンネルでの無効化ですが、*Wall Street Journal* や *Mibbit* など様々なサイトがまだこの弱い暗号を使用していることが判明しています。HTTPS サイトを運営しているウェブマスターの皆さんには [Observatory by Mozilla](https://observatory.mozilla.org/) を使ってサーバー設定を見直すことを推奨します。
