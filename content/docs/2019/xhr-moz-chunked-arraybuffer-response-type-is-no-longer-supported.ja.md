---
title: "XHR `moz-chunked-arraybuffer` レスポンスタイプへの対応が廃止されました"
date: "2019-05-28T06:06:00-04:00"
categories: ["dom"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171"
      title: "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes (moz-blob, moz-chunked-text, and moz-chunked-arraybuffer)"
---
[Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/prefixed-xmlhttprequest-response-types-including-moz-blob-are-no-longer-supported/) 以降廃止予定となっていた、[`XMLHttpRequest.responseType`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseType) プロパティ用の非標準 `moz-chunked-arraybuffer` レスポンスタイプが Firefox 68 で削除されました。代わりに `fetch()` を Firefox 65 以降使用可能な Streams API と組み合わせて使うことができます。詳しくは MDN の [Using readable streams](https://developer.mozilla.org/docs/Web/API/Streams_API/Using_readable_streams) を参照してください。

**更新**: この記事の初版では `arraybuffer` タイプを代替策として言及していましたが、それは間違いでした。フィードバックを受けてこの記事は訂正済みです。
