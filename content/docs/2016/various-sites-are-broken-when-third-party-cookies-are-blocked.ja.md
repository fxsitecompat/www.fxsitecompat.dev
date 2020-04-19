---
title: "サードパーティ Cookie ブロック時に様々なサイトが正しく動作しません"
date: "2016-03-11T12:58:00-05:00"
categories: ["dom", "plugins", "privacy-security"]
tags: []
versions: ["45", "45-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1254856"
      title: "Bug 1254856 - Some websites (forgeofempires.com, bet365.com, inbox.google.com) can't finish loading with \"Accept third-party cookies: Never\" checked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257861"
      title: "Bug 1257861 - Firefox 45 fails to send Cookie header with XHR post requests done from a web worker when third-party cookies are blocked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257236"
      title: "Bug 1257236 - The \"inbox.google.com\" page keeps refreshing on and on with \"Accept third-party cookies: Never\" checked"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1249083"
      title: "Bug 1249083 - Google Sheets not evaluating cells"
aliases:
    - "/ja/docs/2016/some-flash-sites-are-broken-when-third-party-cookies-are-blocked/"
    - "/ja/docs/2016/some-sites-are-broken-when-third-party-cookies-are-blocked/"
    - "/ja/docs/2016/cookies-are-missing-in-xhr-post-requests-from-workers-when-third-party-cookies-are-blocked/"
---
サードパーティ Cookie をブロックするようブラウザーが設定されている場合に、オンラインゲームやライブストリーミング動画など、特定の Flash サイトの読み込みが完了しないというリグレッションが Firefox 45 で発生しました。Mozilla 開発者が解決策に取り組んでいます。

**更新**: コード内の同じバグにより、非 Flash の *Google Inbox* ウェブアプリケーションも正しく動作しないことが確認されました。それを受けてこの記事のタイトルを訂正しました。この問題は Firefox 45.0.1 で修正されました。

**更新**: *Google Inbox* の問題は Firefox 45.0.1 で修正されていないとの報告がユーザーから上がっています。また *Google Sheets* やその他いくつかのサイトもサードパーティ Cookie ブロック時に正常動作しないことが確認されました。私たちはそれらのバグのひとつで、[Worker](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers) 内で行われた [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) POST リクエストが、それらのリソースが [同一配信元](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) にある場合でも HTTP `Cookie` ヘッダーを送信しないとことを発見しました。Mozilla 開発者が詳細を調査中です。

**更新**: このバグは Firefox 45.0.2 で修正されました。
