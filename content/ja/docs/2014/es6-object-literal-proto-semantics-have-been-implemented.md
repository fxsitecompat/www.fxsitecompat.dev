---
title: "ES6 オブジェクトリテラル `__proto__` セマンティクスが実装されました"
date: "2014-10-17T22:50:44-04:00"
categories: ["javascript"]
tags: []
versions: ["35"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1061853": "Bug 1061853 – Implement ES6 object-literal __proto__ restrictions/semantics"
---
ECMAScript 6 の [オブジェクトリテラル内でのプロトタイプ改変](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Object_initializer#Prototype_mutation) に関するセマンティクスと制限が実装されました。今後オブジェクトリテラル内では [`__proto__`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/proto) によるプロトタイプ改変がひとつだけ許容され、複数改変を行おうとした場合 [`SyntaxError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) が投げられます。また、`__proto__() {}` のようなメソッドメンバーがプロトタイプを上書きしなくなりました。
