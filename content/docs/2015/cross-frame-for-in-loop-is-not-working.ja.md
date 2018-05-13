---
title: "クロスフレーム `for-in` ループが動作しません"
date: "2015-10-22T22:58:00-07:00"
categories: ["javascript"]
tags: []
versions: ["37"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1152550"
      title: "Bug 1152550 - Cross-frame for-in is broken on Firefox 37, 38 beta"
---
Firefox 37 には、[`for...in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...in) 命令文がクロスフレームオブジェクト上で動作せず、`TypeError` を投げるというリグレッションがあります。*Google Caja* を使っている一部のサイトが影響を受けている可能性があります。この問題は Firefox 38 で修正されました。
