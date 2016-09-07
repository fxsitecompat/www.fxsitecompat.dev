---
title: "`for-each-in` ループ対応が廃止されます"
date: "2015-10-25T23:45:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=824289"
      title: "Bug 824289 - Hide \"for each\" from web content regardless of the JS version"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293205"
      title: "Bug 1293205 - Warn about non-standard for-each regardless of JS version number"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293305"
      title: "Bug 1293305 - Disable non-standard for-each on nightly-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083470"
      title: "Bug 1083470 - Remove SpiderMonkey support for E4X for-each"
---
[Firefox 37 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2015/for-each-in-loops-are-now-deprecated/) [`for each...in`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for_each...in) 命令文は、ECMAScript 2015 (ES6) 仕様に含まれていないため、近い将来削除されることとなりました。代わりに標準の [`for...of`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/for...of) 命令文を使用してください。

**更新**: Firefox 51 以降では、JavaScript のバージョンに関わらず `for-each-in` に関する警告がコンソールに表示されます。この非標準命令文は近々 Firefox Nightly で無効化されます。
