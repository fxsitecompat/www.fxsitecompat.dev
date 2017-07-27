---
title: "分割代入型 `for-in` ループが削除されました"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083498"
      title: "Bug 1083498 - Remove SpiderMonkey support for destructuring for-in (JS1.7-only language extension)"
---
JavaScript 1.7 に含まれていた、`for (var/let/const [key, value] in object)` のような分割代入型 [`for...in`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...in) ループの非標準実装が削除されました。[配列](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array) や他の [反復可能オブジェクト](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Iteration_protocols) に関しては、単純に [`for...of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) ループで代用可能です。一般的な [オブジェクト](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object) に関しても、`for (let [key, value] of Iterator(object))` のように [`Iterator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Iterator) との組み合わせで `for...of` ループを使用できますが、残念ながらこの非標準 `Iterator` も将来的に削除されます。そのため、現実的な解決策は `for (let key in obj) { let value = obj[key]; }` のようになるでしょう。
