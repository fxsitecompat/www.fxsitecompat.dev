---
title: "Web Crypto API が安全でないサイト上では使用できなくなります"
date: "2018-06-05T10:54:00-04:00"
categories: ["misc", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333140"
      title: "Bug 1333140 - Require [SecureContext] for Web Crypto"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/55t-Uyx1TxI/discussion"
      title: "Intent to Remove: Insecure use of WebCrypto"
---
[Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) は近々、現行の仕様で求められている通り、HTTPS 経由で配信された安全なサイトのみで動作するようになります。2017 年 7 月公開の [Google Chrome 60](https://developers.google.com/web/updates/2017/06/chrome-60-deprecations) で既にこの変更が行われていることから、互換性リスクは低いはずです。
