---
title: "値を伴わない `yield` は非推奨となりました"
date: "2013-07-14T19:12:37-04:00"
categories: ["javascript"]
tags: []
versions: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=885463"
      title: "Bug 885463 – Warn about \'yield\' without operand"
---
[`yield`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/yield) 演算子をオペランド (値) なしに使うことができなくなりました。この変更は [ECMAScript 6](https://developer.mozilla.org/docs/JavaScript/ECMAScript_6_support_in_Mozilla) 仕様準拠のため行われたもので、コード内で値が指定されていない場合は [ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) 内に警告が表示されます。返す値が特にない場合は、代わりに `yield undefined` を使えば良いでしょう。
