---
title: "`window.crypto` の未実装メソッドが削除されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=897359": "Bug 897359 – Remove unimplemented method in nsCrypto"
---
[`window.crypto`](https://developer.mozilla.org/ja/docs/Web/API/window.crypto) から、`disableRightClick`、[`popChallengeResponse`](https://developer.mozilla.org/ja/docs/JavaScript_crypto/popChallengeResponse)、`random` メソッドが削除されました。これらは Netscape 4 の非標準 [Crypto API](https://developer.mozilla.org/ja/docs/JavaScript_crypto) の一部でしたが、[Gecko](https://developer.mozilla.org/ja/docs/Mozilla/Gecko) ベースの Netscape 6 や Firefox には実装されておらず、例外 `NS_ERROR_NOT_IMPLEMENTED` を投げるだけでした。なお、暗号学的にランダムな値を得るには、標準化された [`window.crypto.getRandomValues`](https://developer.mozilla.org/ja/docs/Web/API/window.crypto.getRandomValues) が [Firefox 21](https://developer.mozilla.org/ja/Mozilla/Firefox/Releases/21) 以降使用可能です。
