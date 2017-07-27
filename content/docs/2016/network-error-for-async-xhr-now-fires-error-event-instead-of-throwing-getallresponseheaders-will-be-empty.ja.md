---
title: "非同期 XHR のネットワークエラーが例外の代わりに `error` イベントを発生させるようになり、`getAllResponseHeaders` は空文字列を返します"
date: "2016-08-01T00:04:00-04:00"
categories: ["dom"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=709991"
      title: "Bug 709991 - [XHR2] Cross-origin XHR with username/password in URL throws"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1286744"
      title: "Bug 1286744 - [XHR2] GetAllResponseHeaders() should return an empty string if the XHR failed."
aliases:
    - "/ja/docs/2016/network-error-for-async-xhr-now-fires-error-event-instead-of-throwing/"
---
従来 Firefox は、非同期 [`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) のネットワークエラーを検出した際に `NetworkError` 例外を投げていました。Firefox 50 以降では、Firefox 45 以降 [クロスオリジンのワーカー読み込みが `error` イベントを発生させている](https://www.fxsitecompat.com/ja/docs/2016/loading-cross-origin-worker-now-fires-error-event-instead-of-throwing-worker-in-sandboxed-iframe-no-longer-allowed/) のと同様に、ブラウザーは [`error`](https://developer.mozilla.org/ja/docs/Web/Events/error) イベントを非同期で発生させるようになります。以下のように [`onerror`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequestEventTarget/onerror) ハンドラーを [`try-catch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/try...catch) 宣言と組み合わせて使うことで、両方の場合に適切に対処できます。

```js
var xhr = new XMLHttpRequest();
xhr.addEventListener('load', function (event) {
  // ...
});
xhr.addEventListener('error', function (event) {
  // 新しいブラウザー向けにネットワークエラーを処理
});
xhr.open('GET', url, true);
try {
  xhr.send(null);
} catch (ex) {
  // 古いブラウザー向けにネットワークエラーを処理
}
```

なお、同期 `XMLHttpRequest` は引き続き例外を投げます。

これと関連し、[`XMLHttpRequest.getAllResponseHeaders`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest/getAllResponseHeaders) メソッドは、ネットワークエラーが発生した場合に空文字列を返すようになりました。
