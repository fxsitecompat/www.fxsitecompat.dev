---
title: "接頭辞付き `XMLHttpRequest` レスポンスタイプが削除されます"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171": "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes"
---
[`XMLHttpRequest.responseType`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest#xmlhttprequest-responsetype) によって返される、非標準で `moz` 接頭辞が付いているいくつかの値、具体的には `moz-blob`、`moz-chunked-text`、`moz-chunked-arraybuffer` について、削除が検討されています。
