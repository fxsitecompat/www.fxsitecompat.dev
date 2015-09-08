---
title: "括弧付き分割代入パターンは使用できなくなりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1146136": "Bug 1146136 - Parenthesized AssignmentPatterns are not a valid LHS"
---
ES6 仕様準拠の一環として、`([a, b]) = [1, 2]` や `({a, b}) = { a: 1, b: 2 }` のような括弧付き分割代入パターンは無効なコードと見なされ、[`SyntaxError`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) が投げられるようになりました。詳しくは [Jeff Walden のブログ記事](http://whereswalden.com/2015/06/20/new-changes-to-make-spidermonkeys-and-firefoxs-parsing-of-destructuring-patterns-more-spec-compliant/) を参照してください。
