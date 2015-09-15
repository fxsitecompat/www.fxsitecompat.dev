---
title: "旧式 Crypto API が無効化されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: "33"
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1036546": "Bug 1036546 – soft-disable proprietary window.crypto functions/properties before removing them entirely "
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1083118": "Bug 1083118 – window.crypto.signText replacement"
---
[`window.crypto`](https://developer.mozilla.org/ja/docs/Web/API/window.crypto) 上に実装されていた Netscape 由来の [旧式 Crypto API](https://developer.mozilla.org/ja/docs/JavaScript_crypto) が無効化されました。対象となるのは、`enableSmartCardEvents`、`version` 両プロパティに加え、`generateCRMFRequest`、`importUserCertificates`、`logout`、`signText` の各メソッドです。これらの機能は一度も標準化されたことはなく、一方で標準の [Web Crypto API の実装が進んでいる](https://bugzilla.mozilla.org/show_bug.cgi?id=865789) ことから、Firefox 34 で削除されます。詳しくは [MozillaWiki の記事](https://wiki.mozilla.org/SecurityEngineering/Removing_Proprietary_window.crypto_Functions) を参照してください。

**更新**: Firefox 33 について寄せられたフィードバックにより、多くの銀行や政府機関でこの旧式 Crypto API、特に `crypto.signText` メソッドが未だに使用されていることが明らかになりました。そのため Mozilla は、Firefox 34 でこの API を復活させ、近い将来に代替となる Firefox 拡張機能が拡張され次第、改めて削除することを決定しました。Firefox 33 ユーザは、設定 `dom.unsafe_legacy_crypto.enabled` を `true` にすることで、API を再度有効化できます。また Firefox 31 ESR ユーザはこの変更による影響を受けません。

**更新**: 旧式 Crypto API は [Firefox 35 で削除されました](https://www.fxsitecompat.com/ja/docs/2014/legacy-crypto-api-has-been-removed/)。
