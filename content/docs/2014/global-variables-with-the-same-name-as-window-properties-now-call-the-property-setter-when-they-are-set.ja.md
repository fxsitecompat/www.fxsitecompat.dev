---
title: "`window` プロパティと同名のグローバル変数が、設定時にそのプロパティセッターを呼び出すようになりました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=932322"
      title: "Bug 932322 – Make Window\'s WebIDL properties be own properties of window"
---
この変更の典型的な影響が [Bug 943958](https://bugzilla.mozilla.org/show_bug.cgi?id=943958) で報告されています。`var name = 1` のようなコードは期待通り動作しなくなり、`name` は代わりに文字列の `"1"` を返すようになります。なぜなら [`window.name`](https://developer.mozilla.org/docs/Web/API/window.name) プロパティが存在するためです。これは WebKit や Blink と同じ挙動になります。ウェブ開発者は [`window`](https://developer.mozilla.org/docs/Web/API/window) プロパティと同名のグローバル変数の使用を常に避けるべきです。
