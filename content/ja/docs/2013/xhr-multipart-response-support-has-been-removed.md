---
title: "XHR マルチパートレスポンス対応が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: ["22"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=843508"
      title: "Bug 843508 – Remove support for multipart XHR responses"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/iuKw5doD5Ho/discussion"
      title: "Chrome removed support for multipart/x-mixed-replace documents. We should too."
---
[`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) から、[Firefox 20 以降廃止予定となっていた](https://www.fxsitecompat.com/ja/docs/2012/xhr-multipart-support-is-now-deprecated/) `multipart` プロパティと `multipart/x-mixed-replace` レスポンスの対応が削除されました。これは Firefox 独自機能で標準化されることはありませんでした。[サーバ送信イベント](https://developer.mozilla.org/ja/docs/Server-sent_events)、[Web Sockets](https://developer.mozilla.org/ja/docs/WebSockets)、あるいは進捗イベントからの `responseText` 調査で代用してください。
