---
title: "`hasFeature`/`isSupported` メソッドが常に `true` を返すようになりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: "19"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=801425": "Bug 801425 – Make hasFeature() and isSupported() always return true"
---
[`document.implementation`](https://developer.mozilla.org/ja/docs/DOM/document.implementation).hasFeature と [`Element.isSupported`](https://developer.mozilla.org/ja/docs/DOM/Element.isSupported) の両メソッドが常に `true` を返すようになりました。これらは役に立たない API とみなされ仕様が変更されました。ただし SVG 機能に関しては例外で、従来通り実際の対応状況が返ります。
