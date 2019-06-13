---
title: "`unload`、`pagehide` イベント中の同期 XHR の使用は非推奨となりました"
date: "2019-06-09T03:55:00-04:00"
categories: ["dom"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=980902"
      title: "Bug 980902 - Warn about use of sync XHR during unload and pagehide events"
---
Firefox 68 以降、同期 `XMLHttpRequest` が `unload` あるいは `pagehide` イベントリスナー内で使われていた場合、ユーザー体験を損なうことから、ウェブコンソールが警告を表示します。すべてのモダンブラウザーで使用可能となっている [`navigator.sendBeacon`](https://developer.mozilla.org/docs/Web/API/Navigator/sendBeacon) メソッドを代わりに使ってください。

なお、[Firefox 30](https://www.fxsitecompat.dev/ja/docs/2014/synchronous-xmlhttprequest-has-been-deprecated/) 以降、これらのイベント外での同期 `XMLHttpRequest` の使用に対しては警告が出されています。メインスレッド上でのリクエストがすべて非同期となっているかどうか、あなたのコードを再確認した方が良いでしょう。
