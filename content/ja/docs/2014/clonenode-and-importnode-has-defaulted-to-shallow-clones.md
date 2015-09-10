---
title: "`cloneNode` と `importNode` の既定動作が浅い複製になりました"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: "29"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=937461": "Bug 937461 – Make cloneNode/importNode with the \"deep\" arg not passed default to shallow cloning"
---
[`Node.cloneNode`](https://developer.mozilla.org/ja/docs/Web/API/Node.cloneNode)、[`document.importNode`](https://developer.mozilla.org/ja/docs/Web/API/document.importNode) 両メソッドは真偽値の `deep` 引数を取ります。これは DOM4 の仕様ではオプションであり、省略された場合、これらのメソッドは `deep` の値が `true` であるとみなします。しかしこの挙動が最新の仕様で変更され、省略された場合、この値が `false` であるとみなされるようになりました。実装は Firefox 29 で変更され、深い複製に代わって浅い複製が既定動作になりました。[Firefox 28](https://www.fxsitecompat.com/ja/docs/2013/make-sure-the-deep-argument-is-specified-for-clonenode-and-importnode/) は、後方互換性と前方互換性どちらのためにも、この引数を省略しないようコンソールを通じて開発者に警告を出していました。
