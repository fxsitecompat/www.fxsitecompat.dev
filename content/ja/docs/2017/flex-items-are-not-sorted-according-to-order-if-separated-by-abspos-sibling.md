---
title: "可変アイテムが絶対配置要素で分離された場合、`order` に従って並べ替えられません"
date: "2017-03-14T20:13:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1345873"
      title: "Bug 1345873 - flex items aren't sorted according to \"order\", if they're separated by an abspos sibling"
---
Firefox 52 では、可変アイテムが以下のように絶対配置された要素で分離されると、それらのアイテムを任意の順番で並べ替えられる CSS [`order`](https://developer.mozilla.org/ja/docs/Web/CSS/order) プロパティが無視されてしまう場合があります。

```html
<div style="display:flex">
  <div style="order:2">B</div>
  <div style="position:absolute"></div>
  <div style="order:1">A</div>
</div>
```

Mozilla 開発者はこのリグレッションを認識しており、解決策に取り組んでいます。
