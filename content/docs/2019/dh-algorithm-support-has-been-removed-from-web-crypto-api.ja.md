---
title: "Web Crypto API から DH アルゴリズム対応が削除されました"
date: "2019-11-14T07:33:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1564509"
      title: "Bug 1564509 - Remove support for DH from WebCrypto API (not in spec)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Ut3-eQmUdWg/discussion"
      title: "Intent-to-Unship: DH algorithm support for WebCrypto"
---
Firefox 72 で [`SubtleCrypto.generateKey`](https://developer.mozilla.org/docs/Web/API/SubtleCrypto/generateKey) メソッドからディフィー・ヘルマン (DH) 鍵共有アルゴリズムへの対応が削除されました。これは [Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) の最終仕様に含まれていないためです。Firefox がこのアルゴリズムに対応している唯一のブラウザーであり、Mozilla 開発者によれば使用率は非常に低いことから、互換性への影響は軽微なはずです。
