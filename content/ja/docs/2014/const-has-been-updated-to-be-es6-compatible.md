---
title: "`const` が更新され ES6 準拠となりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=611388": "Bug 611388 – const should be block-scoped and an initializer should be required"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1095439": "Bug 1095439 – Assigning to a const variable is a syntax error"
---
[`const`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/const) 命令文の対応が更新され、ECMAScript 6 仕様準拠となりました。まず、[`let`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let) 命令文のようにブロックスコープ化されたため、`{ const a = 1 }; a;` のようなコードは単に `1` を返さず [`ReferenceError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError) を投げるようになります。次に、初期化子が必要となったため、例えば `const a;` は [`SyntaxError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) を投げます。また、再宣言ができなくなったため、`const a = 1; a = 2;` も同じく `SyntaxError` を投げます。
