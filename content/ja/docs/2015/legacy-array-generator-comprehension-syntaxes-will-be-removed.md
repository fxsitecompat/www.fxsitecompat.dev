---
title: "古い配列・ジェネレータ内包構文が削除されます"
date: "2015-11-02T01:48:00-08:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1220564": "Bug 1220564 - Remove legacy array/generator comprehension."
aliases:
    - "/docs/2015/array-generator-comprehensions-will-be-removed/"
---
JavaScript [1.7](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.7) と [1.8](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.8) で導入された古い非標準の [配列内包](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Array_comprehensions) と [ジェネレータ内包](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions) への対応は、近い将来削除されます。ECMAScript に提案されているそれぞれの新しい構文は Firefox 30 以降で使用可能となっています。ただし、それらが標準化されるかどうかは未だ不透明です。

**更新**: このドキュメントの初期草稿では配列・ジェネレータ内包が削除されると記載していましたが、バグが更新され、差し当たり古い構文のみ削除されることになりました。
