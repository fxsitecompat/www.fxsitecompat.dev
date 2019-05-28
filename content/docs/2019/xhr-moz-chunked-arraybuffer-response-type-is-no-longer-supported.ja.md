---
title: "XHR `moz-chunked-arraybuffer` レスポンスタイプへの対応が廃止されました"
date: "2019-05-28T06:06:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171"
      title: "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes (moz-blob, moz-chunked-text, and moz-chunked-arraybuffer)"
---
[Firefox 58](https://www.fxsitecompat.com/ja/docs/2017/prefixed-xmlhttprequest-response-types-including-moz-blob-are-no-longer-supported/) 以降廃止予定となっていた、[`XMLHttpRequest.responseType`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseType) プロパティ用の非標準 `moz-chunked-arraybuffer` レスポンスタイプが Firefox 68 で削除されました。`arraybuffer` で代用してください。
