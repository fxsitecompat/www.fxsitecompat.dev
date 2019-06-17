---
title: "`DOMError` が `DOMException` に置き換えられました"
date: "2017-10-03T04:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120178"
      title: "Bug 1120178 - Remove DOMError"
aliases:
    - "/ja/docs/2017/domerror-has-been-removed-in-favour-of-domexception/"
---
[`DOMError`](https://developer.mozilla.org/docs/Web/API/DOMError) インターフェイスは、DOM4 仕様から削除されたため、Firefox 55 以降エラーに使用されなくなりました。今後、[`FileReader`](https://developer.mozilla.org/docs/Web/API/FileReader)、[`IDBRequest`](https://developer.mozilla.org/docs/Web/API/IDBRequest)、[`IDBTransaction`](https://developer.mozilla.org/docs/Web/API/IDBTransaction) および [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) オブジェクト上の `error` プロパティは [`DOMException`](https://developer.mozilla.org/docs/Web/API/DOMException) を代わりに返すようになります。この変更は、以下のように何らかの理由でオブジェクトタイプを判別していない限り、実際のコードには影響しないはずです。

```js
error instanceof DOMError
```

**更新**: `DOMError` インターフェイスは [Firefox 69](https://www.fxsitecompat.dev/ja/docs/2019/domerror-has-been-completely-removed/) で完全に削除されるまで存在していました。この記事は事実を反映して訂正されています。
