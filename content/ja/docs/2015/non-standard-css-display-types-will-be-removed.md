---
title: "非標準 CSS `display` タイプは削除されます"
date: "2015-10-27T17:21:00-07:00"
categories: ["css"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=879275"
      title: "Bug 879275 - Consider turning off -moz-box display types in untrusted stylesheets"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=914360"
      title: "Bug 914360 - Do not expose XUL Grid (display: -moz-grid;) to Web content"
---
本来 Firefox で使用されている [XUL](https://developer.mozilla.org/ja/docs/Mozilla/Tech/XUL) 向けだった非標準の CSS [`display`](https://developer.mozilla.org/ja/docs/Web/CSS/display) プロパティ値が Web コンテンツから使用できなくなります。これには、`-moz-box`、`-moz-deck`、`-moz-grid`、`-moz-grid-group`、`-moz-grid-line`、`-moz-groupbox`、`-moz-inline-box`、`-moz-inline-grid`、`-moz-inline-stack`、`-moz-popup`、`-moz-stack` が含まれます。代わりに [標準の可変ボックス](https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) を使ってください。
