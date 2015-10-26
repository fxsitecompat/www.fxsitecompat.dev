---
title: "`Iterator` メソッドが削除されます"
date: "2015-10-26T13:56:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=881061": "Bug 881061 - Remove Iterator"
---
[JavaScript 1.7](https://developer.mozilla.org/ja/docs/Web/JavaScript/New_in_JavaScript/1.7) で導入され、あらゆるオブジェクトを [反復可能](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Iterators_and_Generators) にするために使われてきた非標準の [`Iterator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Iterator) メソッドは、将来的に削除されます。これは一度も標準化されたことがなく、他のブラウザにも実装されていません。

ECMAScript 2015 (ES6) は、[`Array`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)、[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`Set`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Set) などいくつかの反復可能なオブジェクトを提供しており、[`StyleSheetList`](https://developer.mozilla.org/ja/docs/Web/API/Document/styleSheets) ([Firefox 31](https://bugzilla.mozilla.org/show_bug.cgi?id=738196) 以降)、[`CSSRuleList`](https://developer.mozilla.org/ja/docs/Web/API/CSSRuleList) ([Firefox 32](https://bugzilla.mozilla.org/show_bug.cgi?id=995664) 以降)、[`URLSearchParams`](https://developer.mozilla.org/ja/docs/Web/API/URLSearchParams) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1085284) 以降)、[`FormData`](https://developer.mozilla.org/ja/docs/Web/API/FormData) ([Firefox 44](https://bugzilla.mozilla.org/show_bug.cgi?id=1127703) 以降) など様々な DOM API も今では反復可能となっています。これらは `Iterator` なしに [`for...of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) 命令文と組み合わせて使うことができます。

汎用 [`Object`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object) は他のオブジェクトと異なり反復可能ではなく、そのため従来からある [`for...in`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...in) 命令文を使ってプロパティを反復する必要があります。
