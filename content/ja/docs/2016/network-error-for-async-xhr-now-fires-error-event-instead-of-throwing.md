---
title: "非同期 XHR のネットワークエラーが例外の代わりに `error` イベントを発生させるようになります"
date: "2016-08-01T00:04:00-04:00"
categories: ["dom"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=709991"
      title: "Bug 709991 - [XHR2] Cross-origin XHR with username/password in URL throws"
---
従来 Firefox は、非同期 [`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) のネットワークエラーを検出した際に `NetworkError` 例外を投げていました。Firefox 50 以降では、Firefox 45 以降 [クロスオリジンのワーカー読み込みが `error` イベントを発生させている](https://www.fxsitecompat.com/ja/docs/2016/loading-cross-origin-worker-now-fires-error-event-instead-of-throwing-worker-in-sandboxed-iframe-no-longer-allowed/) のと同様に、ブラウザは [`error`](https://developer.mozilla.org/ja/docs/Web/Events/error) イベントを非同期で発生させるようになります。以下のように [`onerror`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequestEventTarget/onerror) ハンドラを [`try-catch`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Statements/try...catch) 宣言と組み合わせて使うことで、両方の場合に適切に対処できます。

```js
var xhr = new XMLHttpRequest();
xhr.addEventListener('load', function (event) {
  // ...
});
xhr.addEventListener('error', function (event) {
  // 新しいブラウザ向けにネットワークエラーを処理
});
xhr.open('GET', url, true);
try {
  xhr.send(null);
} catch (ex) {
  // 古いブラウザ向けにネットワークエラーを処理
}
```

なお、同期 `XMLHttpRequest` は引き続き例外を投げます。
