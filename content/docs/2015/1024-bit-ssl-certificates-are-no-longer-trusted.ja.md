---
title: "1024 ビット SSL 証明書の信頼が打ち切られました"
date: "2015-02-27T04:21:22-05:00"
categories: ["privacy-security"]
tags: []
versions: ["38"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881553"
      title: "Bug 881553 - Remove or turn off trust bits for 1024-bit root certs after December 31, 2013"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=936105"
      title: "Bug 936105 - Remove or turn off trust bits for Symantec 1024-bit root certs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=986019"
      title: "Bug 986019 - Turn off SSL and Code Signing trust bits for Equifax 1024-bit roots"
---
[1024 ビットルート証明書廃止](https://blog.mozilla.org/security/2014/09/08/phasing-out-certificates-with-1024-bit-rsa-keys/) の最終段階が Firefox 38 で完了となりました。ブログ記事に書かれている通り、お使いの SSL 証明書に 1024 ビットキーが含まれている場合、もしくは 1024 ビットキーの認証局から発行されている場合、新しい SSL 証明書を入手してウェブサーバー上の古い証明書と入れ替える必要があります。

**更新**: *Equifax Secure Certificate Authority* の 1024 ビットルート証明書が、相当数のサイトに影響することが判明したため、[一時的に再度有効化](https://bugzilla.mozilla.org/show_bug.cgi?id=1155279) されました。
