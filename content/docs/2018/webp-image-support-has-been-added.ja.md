---
title: "WebP 画像対応が追加されました"
date: "2018-11-15T09:40:00-05:00"
categories: ["misc"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1294490"
      title: "Bug 1294490 - Implement WebP image support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503653"
      title: "Bug 1503653 - Enable WebP image support by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ywu0gzoQfRY/discussion"
      title: "Intent to implement and ship: WebP image support"
---
Firefox 65 で Google が開発した [WebP 画像形式](https://en.wikipedia.org/wiki/WebP) への対応が追加されました。Chrome と Opera は 5 年以上対応していましたが、Mozilla はこの新形式に対するいくつかの懸念から初期の実装作業を中止していました。しかし、Microsoft Edge が最近になって対応したことや、WebP 画像しか配信せず正しく表示されないサイトの数が増え続けていることから、Firefox の開発者は態度を変えざるを得ませんでした。

あなたのサイトでブラウザー判別に応じて異なる画像形式を用いている場合は、そのコードを更新して Firefox 65 以降に WebP が配信されるようにしてください。Firefox は画像の HTTP `Accept` リクエストヘッダーとして `image/webp,*/*` を送信しますが、WebP を配信するかどうか決定するにはこちらの方法がお勧めです。なお、新形式に非対応の旧バージョンである Firefox 60 [延長サポート版](https://www.mozilla.org/firefox/organizations/) (ESR) は 2019 年 10 月まで公開されることに注意が必要です。
