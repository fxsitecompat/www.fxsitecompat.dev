---
title: "XHR マルチパート対応が廃止予定となりました"
date: "2012-12-29T08:29:30-05:00"
categories: ["dom"]
tags: []
versions: ["20"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=844792"
      title: "Bug 844792 – Warn about the upcoming removal of multipart support in XHR"
---
[`XMLHttpRequest`](https://developer.mozilla.org/docs/DOM/XMLHttpRequest) の `multipart` プロパティと `multipart/x-mixed-replace` レスポンスの対応が廃止予定となりました。これは Firefox 独自機能で標準化されることはありませんでした。そのため [Firefox 22 で削除されます](https://www.fxsitecompat.dev/ja/docs/2013/xhr-multipart-response-support-has-been-removed/)。[サーバー送信イベント](https://developer.mozilla.org/docs/Server-sent_events)、[Web Sockets](https://developer.mozilla.org/docs/WebSockets)、あるいは進捗イベントからの `responseText` 調査で代用してください。

**更新**: マルチパート対応は [Firefox 22 で削除されました](https://www.fxsitecompat.dev/ja/docs/2013/xhr-multipart-response-support-has-been-removed/)。
