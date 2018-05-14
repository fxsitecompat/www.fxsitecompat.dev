---
title: "`for-each-in` ループが廃止予定となりました"
date: "2015-01-16T09:37:54-05:00"
categories: ["javascript"]
tags: []
versions: ["37"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083467"
      title: "Bug 1083467 – Add console warnings for E4X for-each"
---
[ECMAScript for XML (E4X)](https://developer.mozilla.org/docs/Archive/Web/E4X) 対応の一環として JavaScript 1.6 で導入された [`for each...in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for_each...in) 命令文が廃止予定となり、近い将来削除されることとなりました。代わりに ECMAScript 6 [`for...of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) 命令文の使用を検討してください。なお、E4X 対応自体は既に [Firefox 21 で削除](https://www.fxsitecompat.com/ja/docs/2013/e4x-support-has-been-completely-removed/) されており、この命令文は後方互換性のためだけに残されていました。
