---
title: "非標準の `-moz-user-select` 値が削除されました"
date: "2018-11-21T17:08:00-05:00"
categories: ["css"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492958"
      title: "Bug 1492958 - [css-ui] Unship -moz/webkit-user-select values not supported by other UAs / spec"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/XfKl9Jt7ZQ8/discussion"
      title: "Intent to implement and ship: Unprefix -moz-user-select, unship mozilla-specific values."
---
[`-moz-user-select`](https://developer.mozilla.org/docs/Web/CSS/user-select) CSS プロパティとその `-webkit-user-select` エイリアスから以下の Firefox 固有の値が削除されました。

* `-moz-all`: 代わりに `all` を使ってください
* `-moz-text`: 代わりに `text` を使ってください
* `element`、`elements`、`toggle`、`tri-state`: これらは未実装でした

近い将来 `-moz-none` も削除され、プロパティの接頭辞が外れます。

**更新**: [Firefox 69](https://www.fxsitecompat.dev/ja/docs/2018/non-standard-moz-user-select-values-have-been-removed/) でプロパティの接頭辞が外れました。
