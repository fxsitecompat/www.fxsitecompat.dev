---
title: "サードパーティ Cookie ブロック時に一部サイトが正しく動作しません"
date: "2016-03-11T12:58:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1254856"
      title: "Some websites (forgeofempires.com, bet365.com, inbox.google.com) can't finish loading with \"Accept third-party cookies: Never\" checked"
aliases:
    - "/docs/2016/some-flash-sites-are-broken-when-third-party-cookies-are-blocked/"
---
サードパーティ Cookie をブロックするようブラウザが設定されている場合に、オンラインゲームやライブストリーミング動画など、特定の Flash サイトの読み込みが完了しないというリグレッションが Firefox 45 で発生しました。Mozilla 開発者が解決策に取り組んでいます。

**更新**: コード内の同じバグにより、非 Flash の *Google Inbox* Web アプリケーションも正しく動作しないことが確認されました。それを受けてこの記事のタイトルを訂正しました。この問題は Firefox 45.0.1 で修正されました。

**更新**: *Google Inbox* の問題は Firefox 45.0.1 で修正されていないとの報告がユーザから上がっています。サードパーティ Cookie ブロック時に正しく動作しないサイトが他にもいくつかあります。それに関しては [別の記事](https://www.fxsitecompat.com/ja/docs/2016/cookies-are-missing-in-xhr-post-requests-from-workers-when-third-party-cookies-are-blocked/) を投稿しました。
