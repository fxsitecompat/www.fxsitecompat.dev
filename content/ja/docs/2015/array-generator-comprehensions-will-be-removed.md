---
title: "配列・ジェネレータ内包は削除されます"
date: "2015-11-02T01:48:00-08:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1220564": "Bug 1220564 - Remove non-standard array/generator comprehension."
---
[配列内包](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Array_comprehensions) と [ジェネレータ内包](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions) への対応は将来的に削除されます。これらの構文は Mozilla によって提案されていましたが、ECMAScript での標準化に至りませんでした。配列内包は [`Array.prototype.map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/map)、[`filter`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) メソッドと [アロー関数](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/Arrow_functions) で代用できます。ジェネレータ内包は [`function*`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/function*) 宣言で代用できます。
