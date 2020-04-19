---
title: "`for-each-in` ループ対応が廃止されました"
date: "2017-08-08T07:32:00-04:00"
categories: ["javascript"]
tags: []
releases: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293205"
      title: "Bug 1293205 - Warn about non-standard for-each regardless of JS version number"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1293305"
      title: "Bug 1293305 - Disable non-standard for-each on nightly-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083470"
      title: "Bug 1083470 - Disable SpiderMonkey support for E4X for-each"
aliases:
    - "/ja/docs/2015/for-each-in-loop-support-will-be-removed/"
---
[Firefox 37 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2015/for-each-in-loops-are-now-deprecated/) [`for each...in`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for_each...in) 命令文は、ECMAScript 2015 (ES6) 仕様に含まれていないため、Firefox 57 で削除されました。Nightly チャンネルでは Firefox 53 以降既に無効化されています。標準の [`for...of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) 命令文で代用してください。
