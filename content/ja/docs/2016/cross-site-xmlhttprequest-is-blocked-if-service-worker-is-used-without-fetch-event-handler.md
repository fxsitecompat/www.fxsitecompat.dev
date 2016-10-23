---
title: "Service Worker が `fetch` イベントハンドラーなしに使われた場合にクロスサイト `XMLHttpRequest` がブロックされてしまいます"
date: "2016-02-07T22:27:00-05:00"
categories: ["dom", "networking"]
tags: []
versions: ["44"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1243453"
      title: "Bug 1243453 - Missing Origin header in Cross Origin Request resulting in Cross-Origin Request Blocked"
aliases:
    - "/docs/2016/cross-site-xmlhttprequest-is-blocked-due-to-missing-origin-header/"
---
Firefox 44 で、`XMLHttpRequest` と Service Worker に関するリグレッションが発生しました。サイトが Service Worker を導入していて、その中で [`fetch` イベント](https://developer.mozilla.org/ja/docs/Web/API/FetchEvent) の処理が行われていない場合に [クロスサイト HTTP リクエスト](https://developer.mozilla.org/ja/docs/Web/HTTP/Access_control_CORS) が正しく動作しません。この問題が発生すると、`GET` リクエストに `Origin` ヘッダーが欠落し、結果として不要なプレフライト `OPTIONS` リクエストが行われ、それに失敗した `GET` リクエストが続きます。このバグは Firefox 45 で修正されました。Firefox 44 のための回避策は、次のようにシンプルなイベントリスナーをワーカーコードに追加することです。

```js
self.addEventListener('fetch', function(event) {
  event.respondWith(fetch(event.request));
});
```

**更新**: バグのコメントに応じて、Service Worker API を伴う状況について明確にし、回避策を追加しました。
