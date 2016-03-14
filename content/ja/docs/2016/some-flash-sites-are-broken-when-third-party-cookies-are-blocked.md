---
title: "サードパーティ Cookie ブロック時に一部 Flash サイトが正しく動作しません"
date: "2016-03-11T12:58:00-05:00"
categories: ["plugins", "privacy-security"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1254856": "Bug 1254856 - Some Flash websites (forgeofempires.com, bet365.com) can't finish loading with \"Accept third-party cookies: Never\" checked"
---
サードパーティ Cookie をブロックするようブラウザが設定されている場合に、オンラインゲームやライブストリーミング動画など、特定の Flash サイトの読み込みが完了しないというリグレッションが Firefox 45 で発生しました。Mozilla 開発者が解決策に取り組んでいます。
