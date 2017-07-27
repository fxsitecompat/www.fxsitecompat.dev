---
title: "いくつかの内部 CSS プロパティが削除されました"
date: "2015-10-07T01:49:00-04:00"
categories: ["css"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1207002"
      title: "Bug 1207002 - Restrict MathML-related internal properties to only be accessible in UA sheets"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1211040"
      title: "Bug 1211040 - Restrict -moz-window-{dragging, shadow} to chrome only"
---
[MathML](https://developer.mozilla.org/ja/docs/Web/MathML) やブラウザーテーマ向けに用意されている一部の内部 CSS プロパティがウェブコンテンツから使用できなくなりました。これらには `-moz-math-display`、`-moz-window-dragging`、[`-moz-window-shadow`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-window-shadow) が含まれます。

**更新**: `-moz-window-dragging` プロパティは *Graphene* ランタイムとの互換性問題から [元に戻されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1212607)。
