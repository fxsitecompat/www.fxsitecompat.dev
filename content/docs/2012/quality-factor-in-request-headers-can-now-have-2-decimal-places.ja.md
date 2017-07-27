---
title: "リクエストヘッダーの品質係数が小数点以下 2 桁まで反映されるようになりました"
date: "2012-12-03T03:53:26-05:00"
categories: ["networking"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672448"
      title: "Bug 672448 – Clamp quality factor (\'q\') values to 2 decimal places"
---
Firefox はこれまで品質係数を小数点以下 1 桁で固定していました。品質係数とは、[`Accept-Language`](https://developer.mozilla.org/ja/docs/HTTP/Content_negotiation#The_Accept-Language.3A_header) などの HTTP リクエストヘッダーに含まれる、`q=` に続く数値です。この実装では複数の項目が同じ値となってしまう場合があることから、より明確にするため小数点以下 2 桁まで反映するよう変更されました。
