---
title: "`for-of`/`in` ループヘッダ宣言の初期化子が許容されなくなりました"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: "40"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=748550": "Bug 748550 - Remove InitialiserNoIn[opt] from ... in for(var ... in obj) to help simplify ES6"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1164741": "Bug 1164741 - Add back partial support for |for (var i = 0 in obj);| syntax, ignoring the initializer rather than failing on it"
---
従来、[`for...in`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...in)、[`for...of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) 各命令文は、そのループヘッダ宣言に初期化子を持つことが可能で、`for (var/let/const x = ... in/of ...)` のように記述できました。この構文は ECMAScript 1 から 5 までで誤って許容されていましたが、ECMAScript 6 から削除されました。Firefox では今後そうした初期化子は無視され、例えば `for (var i = 0 in array)` は `for (var i in array)` として解釈されます。
