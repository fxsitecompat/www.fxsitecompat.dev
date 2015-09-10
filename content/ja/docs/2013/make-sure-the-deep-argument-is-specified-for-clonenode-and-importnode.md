---
title: "`cloneNode` と `importNode` の `deep` 引数は必ず指定してください"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom"]
tags: []
versions: "28"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=937465": "Bug 937465 – Add a warning when cloneNode/importNode is used without a boolean argument on a node with children"
---
[`Node.cloneNode`](https://developer.mozilla.org/ja/docs/Web/API/Node.cloneNode)、[`document.importNode`](https://developer.mozilla.org/ja/docs/Web/API/document.importNode) 両メソッドは真偽値の `deep` 引数を取ります。これは DOM4 の仕様ではオプションであり、省略された場合、これらのメソッドは `deep` の値が `true` であるとみなします。しかしこの挙動が最新の仕様で変更され、省略された場合、この値が `false` であるとみなされるようになりました。実装は [Firefox 29 で変更されました](https://www.fxsitecompat.com/ja/docs/2014/clonenode-and-importnode-has-defaulted-to-shallow-clones/)。この引数は依然としてオプションですが、Firefox は、後方、前方互換性のためこの引数を省略しないようコンソールを通じて開発者に警告を出すことにしました。
