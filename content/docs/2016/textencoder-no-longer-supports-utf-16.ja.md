---
title: "`TextEncoder` の UTF-16 対応が打ち切られました"
date: "2016-03-25T18:52:00-04:00"
categories: ["dom"]
tags: []
releases: ["48", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257877"
      title: "Bug 1257877 - Remove support for UTF-16 from TextEncoder"
---
最新の Encoding 標準に従い、UTF-16BE、UTF-16LE エンコーディングへの対応が [`TextEncoder`](https://developer.mozilla.org/docs/Web/API/TextEncoder) インターフェイスから削除されました。[コンストラクター](https://developer.mozilla.org/docs/Web/API/TextEncoder/TextEncoder) はオプションの `utfLabel` 引数を無視するようになり、代わりに常時 UTF-8 が使われます。
