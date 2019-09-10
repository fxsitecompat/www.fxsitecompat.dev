---
title: "全画面表示中は許可リクエストを出せなくなりました"
date: "2019-09-05T06:42:00-04:00"
categories: ["misc"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1412561"
      title: "Bug 1412561 - Add-on installation should be blocked when in full-screen mode"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1522120"
      title: "Bug 1522120 - Exit fullscreen when a permission prompt is shown to the user"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1577478"
      title: "Bug 1577478 - Log warning to website console when permission prompt / full-screen is cancelled"
---
ユーザーをブラウザーの [全画面表示モード](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) に閉じ込めて [許可リクエスト](https://developer.mozilla.org/docs/Web/API/Permissions_API) を承認させようとする様々な既知のサイトが存在します。一度許可を出してしまうと、サイトは迷惑なプッシュ通知を送りつけたり、コンピューターのカメラやマイクにアクセスしたり、ブラウザーに悪質な拡張機能をインストールしたりすることさえ可能となってしまいます。こうしたリスクを軽減するため、Firefox 70 で以下の変更が行われました。

* 全画面表示モードへ入る際、保留となっている許可リクエストがあれば取り消し
* 全画面表示モード実行中に許可リクエストが行われた場合は全画面表示を解除
* 全画面表示モード実行中はアドオンのインストールを禁止 (Firefox 68 以降)

つまり、あなたが独自の動画プレーヤーや没入型ゲームなどに Fullscreen API を使用しているのであれば、全画面表示モードへ入る前に必要な許可リクエストを行わなくてはなりません。そうしないとユーザー体験が損なわれる可能性があります。

開発者により詳しく情報を提供するため、Firefox 71 以降では、許可リクエストや全画面表示モードが取り消された場合、ウェブコンソールに警告が記録されます。
