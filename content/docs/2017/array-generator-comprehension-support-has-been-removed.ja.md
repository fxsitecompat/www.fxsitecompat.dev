---
title: "配列・ジェネレーター内包対応が削除されました"
date: "2017-11-10T10:03:00-05:00"
categories: ["javascript"]
tags: []
releases: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1414340"
      title: "Bug 1414340 - Remove ES draft array/generator comprehensions"
---
[配列内包](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Array_comprehensions) と [ジェネレーター内包](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions) への対応が Firefox 58 で削除されました。
これらは元々 JavaScript 1.7 と 1.8 で導入され、後に [古い非標準構文を置き換える形で](https://www.fxsitecompat.dev/ja/docs/2016/legacy-array-generator-comprehension-syntaxes-have-been-removed/) ECMAScript 2015 草案の一部として提案されていましたが、新しい構文も標準化されることはありませんでした。いずれも他のブラウザーには実装されていないことから、互換性リスクは非常に低いはずです。

配列内包は [`Array.prototype.map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map)、[`filter`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) 両メソッドで置き換えられます。ジェネレーター内包も [ジェネレーター関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function*) で置き換えられます。
