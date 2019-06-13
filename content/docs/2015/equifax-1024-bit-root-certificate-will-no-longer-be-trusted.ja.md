---
title: "Equifax 1024 ビットルート証明書への信頼が打ち切られます"
date: "2015-10-24T22:41:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1156844"
      title: "Bug 1156844 - Turn off Trust bits for Equifax Secure Certificate Authority 1024-bit root certificate"
---
一度無効化されたものの互換性問題により [Firefox 38 で再度有効化された](https://www.fxsitecompat.dev/ja/docs/2015/1024-bit-ssl-certificates-are-no-longer-trusted/) *Equifax Secure Certificate Authority* 1024 ビットルート証明書への信頼が、Firefox 44 で削除されます。もしまだこの認証局によって発行された証明書を使っている場合は、できる限り早く交換してください。そうしないとあなたのサイトは Firefox によってブロックされてしまいます。この変更は、[1024 ビット RSA キーを使ったルート証明書を廃止する](https://blog.mozilla.org/security/2014/09/08/phasing-out-certificates-with-1024-bit-rsa-keys/) Mozilla の計画の最終段階となります。
