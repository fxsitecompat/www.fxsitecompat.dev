---
title: "いくつかの内部 CSS プロパティが削除されました"
date: "2015-10-07T01:49:00-04:00"
categories: ["css"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1207002": "Bug 1207002 - Restrict MathML-related internal properties to only be accessible in UA sheets"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1211040": "Bug 1211040 - Restrict -moz-window-{dragging, shadow} to chrome only"
---
[MathML](https://developer.mozilla.org/ja/docs/Web/MathML) やブラウザテーマ向けに用意されている一部の内部 CSS プロパティが Web コンテンツから使用できなくなりました。これらには `-moz-control-character-visibility`、`-moz-math-display`、`-moz-window-dragging`、[`-moz-window-shadow`](https://developer.mozilla.org/ja/docs/Web/CSS/-moz-window-shadow) が含まれます。
