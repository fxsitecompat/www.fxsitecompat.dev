---
title: "`Function.caller` が、厳格、非同期、ジェネレーター関数について `null` を返すようになりました"
date: "2020-02-13T22:52:00-05:00"
categories: ["javascript"]
tags: []
releases: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610206"
      title: "Bug 1610206 - Restrict functions returned by Function#caller"
---
Firefox 75 で、最新の ECMAScript 仕様提案に準拠するため、[`Function.caller`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/caller) プロパティの挙動が変更されました。これは従来、呼び出し元が [厳格関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode) だった場合は `TypeError` を投げていました。Firefox 75 以降、このプロパティはそうした場合に `null` を返します。同様の変更が、以前は呼び出し元へのアクセスが制限されていなかった [非同期関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/async_function) や [ジェネレーター関数](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function*) にも適用されます。

```js
function x() {
  console.log(x.caller);
}
// 以下の関数はすべて `null` を記録するようになりました
(function s() {
  "use strict";
  x(); // 以前は例外が投げられていました
})();
(async function a() {
  x(); // 以前は `a()` が記録されていました
})();
(function* g() {
  yield x(); // 以前は `g()` が記録されていました
}().next());
```
