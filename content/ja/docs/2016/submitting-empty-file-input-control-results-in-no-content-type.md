---
title: "空のファイル入力コントロール送信時に `Content-Type` が設定されません"
date: "2016-04-11T13:12:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1255735"
      title: "Bug 1255735 - Firefox 45 does not send content-type in empty input[type=file] anymore"
---
空の `<input type="file">` を含む `<form enctype="multipart/form-data">` を送信した場合に、`Content-Type` HTTP ヘッダと、`Content-Disposition` ヘッダ内の `filename` フィールドが含まれず、そのアプリケーションのサーバサイドロジックがフォームデータ解析中に不具合を起こす恐れがあるというリグレッションが Firefox 45 で発生しました。

実際のヘッダ:
```http
Content-Disposition: form-data; name="multipartFileList"
```

期待されるヘッダ:
```http
Content-Type: application/octet-stream
Content-Disposition: form-data; name="multipartFileList"; filename=""
```

このバグは Firefox 45.0.2 で修正されました。
