---
title: "`delete` によって「一時死角」が生まれるようになりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: "36"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1074571": "Bug 1074571 – The delete operator should trigger TDZ"
---
ECMAScript 6 で [`const`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/const) と [`let`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let) 命令文のために定義された「[一時死角](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let#Temporal_dead_zone_and_errors_with_let)」の概念が [`delete`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/delete) 演算子にも適用されるようになりました。ドキュメントに書かれている通り、この演算子が関数内で使われると、以後同名の変数を再宣言することはできず、代わりに [`ReferenceError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError) が投げられます。
