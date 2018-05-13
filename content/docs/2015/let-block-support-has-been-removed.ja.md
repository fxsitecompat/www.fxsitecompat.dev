---
title: "`let` ブロック対応が削除されました"
date: "2015-10-24T22:00:00-07:00"
categories: ["javascript"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1167029"
      title: "Bug 1167029 - Remove SpiderMonkey support for let blocks"
aliases:
    - "/ja/docs/2015/let-block-support-will-be-dropped/"
---
[JavaScript 1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) で導入され [Firefox 36 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2014/let-blocks-and-expressions-have-been-deprecated/) 非標準 [`let` ブロック](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_blocks) への対応が、ECMAScript 2015 (ES6) 仕様準拠のため、Firefox 44 で削除されました。[`let` 式](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_expressions) 対応は既に [Firefox 41 で削除されています](https://www.fxsitecompat.com/ja/docs/2015/let-expression-support-has-been-dropped/)。
