---
title: "旧式イテレータープロトコルが削除されました"
date: "2017-09-20T18:52:00-04:00"
categories: ["javascript"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1098412"
      title: "Bug 1098412 - Remove __iterator__ and the legacy Iterator constructor"
---
[JavaScript 1.7](https://developer.mozilla.org/ja/docs/Web/JavaScript/New_in_JavaScript/1.7) で導入された非標準の旧式イテレータープロトコルへの対応が Firefox 57 で削除されました。これには、[`Iterator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Iterator) コンストラクター、`__iterator__` メソッド、[`StopIteration`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/StopIteration) オブジェクトが含まれます。

ECMAScript 2015 (ES6) は反復可能な [`Array`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)、[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set) オブジェクトを提供しており、[`StyleSheetList`](https://developer.mozilla.org/ja/docs/Web/API/StyleSheetList) ([Firefox 31](https://bugzilla.mozilla.org/show_bug.cgi?id=738196) 以降)、[`CSSRuleList`](https://developer.mozilla.org/ja/docs/Web/API/CSSRuleList) ([Firefox 32](https://bugzilla.mozilla.org/show_bug.cgi?id=995664) 以降)、[`URLSearchParams`](https://developer.mozilla.org/ja/docs/Web/API/URLSearchParams) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1085284) 以降)、[`FormData`](https://developer.mozilla.org/ja/docs/Web/API/FormData) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1127703) 以降)、[`Headers`](https://developer.mozilla.org/ja/docs/Web/API/Headers) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1108181) 以降)、[`NodeList`](https://developer.mozilla.org/ja/docs/Web/API/NodeList)、[`DOMTokenList`](https://developer.mozilla.org/ja/docs/Web/API/DOMTokenList) (いずれも [Firefox 50](https://bugzilla.mozilla.org/show_bug.cgi?id=1290636) 以降) といった様々な DOM API も今では反復可能となっています。

これらのオブジェクトは `Iterator` コンストラクターなしに [`for...of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) 命令文と組み合わせて使うことができます。反復可能ではない汎用オブジェクトに関しては、`Iterator` を新しい標準の [`Object.entries`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) メソッドで単純に置き換えることで、反復可能とすることができます。詳しくは [標準のジェネレーターとイテレーター](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Iterators_and_Generators) を参照してください。
