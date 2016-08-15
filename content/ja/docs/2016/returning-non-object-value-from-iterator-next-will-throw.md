---
title: "`iterator.next()` が非オブジェクト値を返すと例外が投げられます"
date: "2016-08-14T16:17:00-04:00"
categories: ["javascript"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1016936"
      title: "Bug 1016936 - Iteration: throw if the value returned by iterator.next() is not an object"
aliases:
    - "/docs/2016/retuning-non-object-value-by-iterator-next-will-throw/"
---
[イテレータプロトコル](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Iteration_protocols#iterator) では、`next` メソッドは常に `done` と `value` を含む適切なプロパティを伴ったオブジェクトを返す必要があります。Firefox は、ECMAScript 2015 (ES6) 仕様に従い、開発者定義の `next` メソッドによって `false` や `undefined` のような非オブジェクト値が返された場合に `TypeError` を投げるようになりました。
