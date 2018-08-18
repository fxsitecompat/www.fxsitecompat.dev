---
title: "`__defineGetter__()` や `__defineSetter__()` をグローバルスコープで呼び出すことはできなくなりました"
date: "2016-03-12T19:11:00-05:00"
categories: ["javascript"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1253016"
      title: "Bug 1253016 - Remove legacy __defineGetter__/__defineSetter__ this behavior"
---
従来、[`__defineGetter__`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__)、[`__defineSetter__`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__) 両メソッドは、グローバルスコープでオブジェクト抜きに呼び出すことが可能でした。なぜなら、そうした場合はグローバルオブジェクトが自動的に使われていたからです。ECMAScript 2016 (ES7) 準拠の一環として、Firefox 48 以降はこの古い挙動に対応せず、代わりに `TypeError` を投げます。ここでの回避策は、`this.__defineGetter__` あるいは `this.__defineSetter__` のように、明示的に [`this`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/this) キーワードを使うことです。
