---
title: "サードパーティ Cookie ブロック時にワーカー内 XHR POST リクエストが Cookie を送信しません"
date: "2016-03-23T17:59:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257861"
      title: "Bug 1257861 - Firefox 45 fails to send Cookie header with XHR post requests done from a web worker when third-party cookies are blocked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257236"
      title: "Bug 1257236 - The \"inbox.google.com\" page keeps refreshing on and on with \"Accept third-party cookies: Never\" checked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249083"
      title: "Bug 1249083 - Google Sheets not evaluating cells"
---
サードパーティ Cookie をブロックするようブラウザが設定されている場合に、[ワーカー](https://developer.mozilla.org/ja/docs/Web/API/Web_Workers_API/Using_web_workers) 内で行われた [`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest) POST リクエストが、それらのリソースが [同一配信元](https://developer.mozilla.org/ja/docs/Web/Security/Same-origin_policy) にある場合でも HTTP `Cookie` ヘッダを送信しないというリグレッションが Firefox 45 で発生しました。これは Firefox 45.0.1 で修正された [別のサードパーティ Cookie 問題](https://www.fxsitecompat.com/ja/docs/2016/some-sites-are-broken-when-third-party-cookies-are-blocked/) と関連があるようです。Mozilla 開発者が解決策に取り組みます。

**更新**: 最近報告されたバグによれば、この問題は *Google Inbox* と *Google Sheets* にも影響しています。
