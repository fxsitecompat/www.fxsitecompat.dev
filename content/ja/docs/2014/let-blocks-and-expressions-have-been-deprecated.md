---
title: "`let` ブロックと `let` 式が廃止予定となりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1023609": "Bug 1023609 – Delete support for let blocks and let expressions for ES6"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1102131": "Bug 1102131 – Log warnings and collect telemetry for deprecated let blocks and let expressions"
---
非標準の [`let` ブロックと `let` 式](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/let#Non-standard_let_extensions) が廃止予定となりました。これら `let` 拡張機能への対応は、現時点では [Web コンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) に警告が表示されていますが、近い将来 Firefox から削除されます。

**更新**: `let` 式への対応は [Firefox 41 で削除されました](https://www.fxsitecompat.com/ja/docs/2015/let-expression-support-has-been-dropped/)。
