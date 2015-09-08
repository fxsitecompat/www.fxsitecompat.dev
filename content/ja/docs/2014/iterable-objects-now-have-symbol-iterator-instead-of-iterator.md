---
title: "列挙可能オブジェクトが `\"@@iterator\"` の代わりに `Symbol.iterator` を持つようになりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: "36"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=918828": "Bug 918828 – Use @@iterator symbol instead of placeholder string"
---
[`Array`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)、[`Map`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Map)、[`NodeList`](https://developer.mozilla.org/ja/docs/Web/API/NodeList) など [列挙可能オブジェクト](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/The_Iterator_protocol) 上の `"@@iterator"` プロパティが、ECMAScript 6 草案で定義された通り [`Symbol.iterator`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator) プロパティに置き換えられました。
