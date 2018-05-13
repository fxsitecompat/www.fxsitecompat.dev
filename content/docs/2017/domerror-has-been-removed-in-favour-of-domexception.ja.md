---
title: "`DOMError` が `DOMException` に置き換えられる形で廃止されました"
date: "2017-10-03T04:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120178"
      title: "Bug 1120178 - Remove DOMError"
---
[`DOMError`](https://developer.mozilla.org/docs/Web/API/DOMError) インターフェイスは、DOM4 仕様で標準化されなくなったことから、Firefox 58 で削除されました。今後、[`FileReader`](https://developer.mozilla.org/docs/Web/API/FileReader)、[`IDBRequest`](https://developer.mozilla.org/docs/Web/API/IDBRequest)、[`IDBTransaction`](https://developer.mozilla.org/docs/Web/API/IDBTransaction) および [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) オブジェクト上の `error` プロパティは [`DOMException`](https://developer.mozilla.org/docs/Web/API/DOMException) を代わりに返すようになります。この変更は、以下のように何らかの理由でオブジェクトタイプを判別していない限り、実際のコードには影響しないはずです。

```js
error instanceof DOMError
```
