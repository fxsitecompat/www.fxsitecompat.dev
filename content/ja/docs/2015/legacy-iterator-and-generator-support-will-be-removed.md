---
title: "古いイテレーター、ジェネレーター対応が廃止されます"
date: "2015-10-26T13:56:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=881061"
      title: "Bug 881061 - Remove Iterator"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083482"
      title: "Bug 1083482 - Remove SpiderMonkey support for JS1.7 legacy generators"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1104014"
      title: "Bug 1104014 - Disable old-style generators in web content"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119777"
      title: "Bug 1119777 - Remove non-standard Function.prototype.isGenerator"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1199296"
      title: "Bug 1199296 - Don't allow legacy generator yield in method definitions"
aliases:
    - "/docs/2015/iterator-method-will-be-removed/"
---
[JavaScript 1.7](https://developer.mozilla.org/ja/docs/Web/JavaScript/New_in_JavaScript/1.7) で導入された非標準のイテレーター、ジェネレーター対応は将来的に削除されます。これらには、[`Iterator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Iterator) オブジェクト、`__iterator__` メソッド、[`StopIteration`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/StopIteration) オブジェクト、[`Function.prototype.isGenerator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Function/isGenerator) メソッド、[古いジェネレーター関数命令文](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/Legacy_generator_function)、[古いジェネレーター関数式](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Legacy_generator_function)、[古いジェネレーターオブジェクト](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Generator#Legacy_generator_objects)、[ジェネレーター内包](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Generator_comprehensions) が含まれます。それぞれの置き換え例に関しては [標準のジェネレーターとイテレーター](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Iterators_and_Generators) を参照してください。

ECMAScript 2015 (ES6) は、[`Array`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)、[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set) などいくつかの反復可能なオブジェクトを提供しており、[`StyleSheetList`](https://developer.mozilla.org/ja/docs/Web/API/Document/styleSheets) ([Firefox 31](https://bugzilla.mozilla.org/show_bug.cgi?id=738196) 以降)、[`CSSRuleList`](https://developer.mozilla.org/ja/docs/Web/API/CSSRuleList) ([Firefox 32](https://bugzilla.mozilla.org/show_bug.cgi?id=995664) 以降)、[`URLSearchParams`](https://developer.mozilla.org/ja/docs/Web/API/URLSearchParams) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1085284) 以降)、[`FormData`](https://developer.mozilla.org/ja/docs/Web/API/FormData) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1127703) 以降) など様々な DOM API も今では反復可能となっています。これらは `Iterator` なしに [`for...of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) 命令文と組み合わせて使うことができます。反復可能ではない汎用オブジェクトに関しては、非標準の `Iterator` オブジェクトを新しい標準の [`Object.entries`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) メソッドで単純に置き換えることで、反復可能とすることができます。
