---
title: "ブラウザーウィンドウの最小幅が設定されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["misc"]
tags: []
versions: ["29"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=897160"
      title: "Bug 897160 – Set a minimum width for the Firefox window"
---
Firefox 29 で導入された新しい [Australis テーマ](https://blog.mozilla.org/ux/2014/04/the-new-face-of-firefox/) で UI が欠けてしまう潜在的な問題を防ぐため、Firefox のデスクトップブラウザーウィンドウに最小幅が設定されました。このサイズは OS X 上で `425px`、他の OS 上で `390px` となっています。これまでモバイルサイトをテストするためにウィンドウをリサイズしていた場合は、便利な [レスポンシブデザインビュー](https://developer.mozilla.org/docs/Tools/Responsive_Design_View) で代用できます。この最小幅はポップアップウィンドウには適用されないため、コンテンツの表示には影響しないはずです。
