---
title: "`XMLHttpRequest` が大きな blob を破損データとして返す場合があります"
date: "2017-03-27T13:11:00-04:00"
categories: ["dom"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1349862"
      title: "Bug 1349862 - XMLHttpRequest returning corrupt data for large blobs"
---
[レスポンスタイプ](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest/responseType) が `blob` の大きなデータを `XMLHttpRequest` で取得した結果、破損したファイルが返ってしまう場合があるというリグレッションが Firefox 52 で発生しました。この問題は競合状態によって 10 MB 以上のファイルについて発生するようで、バグの報告者によれば、レスポンスタイプを `moz-blob` に設定することで回避可能です。Mozilla 開発者が解決策を模索しています。

**更新**: この問題は Firefox 53 で修正されました。
