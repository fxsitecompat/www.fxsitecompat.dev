---
title: "`let` 式への対応が削除されました"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
releases: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1023609"
      title: "Bug 1023609 - Remove SpiderMonkey support for let expressions"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1167029"
      title: "Bug 1167029 - Remove SpiderMonkey support for let blocks"
---
[JavaScript 1.7](https://developer.mozilla.org/docs/Web/JavaScript/New_in_JavaScript/1.7) で導入され [Firefox 36 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2014/let-blocks-and-expressions-have-been-deprecated/) 非標準 [`let` 式](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_expressions) への対応が、ECMAScript 6 仕様準拠のため削除されました。[`let` ブロック](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#let_blocks) 対応もまもなく削除されます。
