---
title: "`FetchEvent.isReload` が廃止されました"
date: "2020-01-26T20:38:00-05:00"
categories: ["dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1264175"
      title: "Bug 1264175 - Remove FetchEvent.isReload"
---
`FetchEvent` インターフェイス上の [`isReload`](https://developer.mozilla.org/docs/Web/API/FetchEvent/isReload) プロパティが、遡ること 2017 年に Service Workers 仕様から外されているため、Firefox 74 で削除されました。代わりに `Request` インターフェイス上の [`cache`](https://developer.mozilla.org/docs/Web/API/Request/cache) プロパティを使って、その値が `reload` かどうかを確認できます。

```js
// 非推奨
if (event.isReload) { ... }
// 推奨
if (event.request.cache === 'reload') { ... }
```
