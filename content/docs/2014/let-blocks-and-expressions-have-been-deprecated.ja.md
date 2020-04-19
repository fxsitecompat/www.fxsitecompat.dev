---
title: "`let` ブロックと `let` 式が廃止予定となりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
releases: ["36", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1023609"
      title: "Bug 1023609 – Delete support for let blocks and let expressions for ES6"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1102131"
      title: "Bug 1102131 – Log warnings and collect telemetry for deprecated let blocks and let expressions"
---
非標準の [`let` ブロックと `let` 式](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#Non-standard_let_extensions) が廃止予定となりました。これら `let` 拡張機能への対応は、現時点では [ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) に警告が表示されていますが、近い将来 Firefox から削除されます。

**更新**: `let` 式への対応は [Firefox 41 で削除されました](https://www.fxsitecompat.dev/ja/docs/2015/let-expression-support-has-been-dropped/)。

**更新**: `let` ブロックへの対応は早くて [Firefox 44 で削除されます](https://www.fxsitecompat.dev/ja/docs/2015/let-block-support-will-be-dropped/)。
