---
title: "`Headers.getAll` が削除され、代わりに `get` がすべての値を返すようになります"
date: "2016-11-16T15:51:00-05:00"
categories: ["dom"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1278275"
      title: "Bug 1278275 - Headers.get should incorporate getAll behaviour"
---
[`Headers.prototype.getAll`](https://developer.mozilla.org/docs/Web/API/Headers/getAll) メソッドが、最新の Fetch 仕様に従って削除されました。代わりに、[`Headers.prototype.get`](https://developer.mozilla.org/docs/Web/API/Headers/get) メソッドが、指定された HTTP ヘッダーについて、最初の値だけでなくすべての値をコンマ区切りの文字列で返すようになりました。

```js
const headers = new Headers();
headers.append('Accept-Language', 'en');
headers.append('Accept-Language', 'fr');

// Firefox 51 以前
headers.get('Accept-Language'); // "en"
headers.getAll('Accept-Language'); // ["en", "fr"]

// Firefox 52 以降
headers.get('Accept-Language'); // "en,fr"
```
