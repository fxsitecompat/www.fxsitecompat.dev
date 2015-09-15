---
title: "ES6 準拠の `let` で変数の再宣言が許容されなくなりました"
date: "2014-10-17T22:50:44-04:00"
categories: ["javascript"]
tags: []
versions: "35"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1001090": "Bug 1001090 – Implement ES6 \"temporal dead zone\" for let"
---
[`let`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let) 命令文の実装が更新され、ECMAScript 6 仕様の「[temporal dead zone (一時死角)](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let#Temporal_dead_zone_and_errors_with_let)」への対応が行われました。ただし、実装はまだ ES6 完全準拠とはなっていません。Firefox 35 以降、同一ブロックスコープ内で既存関数が再宣言された場合は [`TypeError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/TypeError) が、変数の宣言前にその変数が参照された場合は [`ReferenceError`](https://developer.mozilla.org/ja/docs/JavaScript/Reference/Global_Objects/ReferenceError) が例外として投げられます。この変更は主に Firefox や Firefox OS 向けの [Open Web Apps](https://developer.mozilla.org/ja/docs/Web/Apps)、そして [Firefox 拡張機能](https://developer.mozilla.org/ja/docs/Mozilla/Add-ons) に影響します。詳しくは [ニュースグループでの発表](https://groups.google.com/forum/#!topic/mozilla.dev.platform/tezdW299Zds) も参照してください。
