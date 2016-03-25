---
title: "`TextEncoder` の UTF-16 対応が打ち切られました"
date: "2016-03-25T18:52:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257877"
      title: "Bug 1257877 - Remove support for UTF-16 from TextEncoder"
---
レガシーな `utf-16be`、`utf-16le` エンコーディングへの対応が [`TextDecoder`](https://developer.mozilla.org/ja/docs/Web/API/TextDecoder) インタフェースから削除されました。代わりに `utf-8` を使用してください。
