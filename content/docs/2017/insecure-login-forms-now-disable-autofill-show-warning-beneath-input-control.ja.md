---
title: "安全でないログインフォームで自動補完が無効となり、入力コントロール直下に警告が表示されるようになりました"
date: "2017-01-19T12:25:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1217152"
      title: "Bug 1217152 - Flip prefs to disable login autofill on HTTP and enable the warning on insecure login fields"
---
現在進行中の [安全でない HTTP 廃止](https://www.fxsitecompat.dev/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、[安全でないパスワード入力に対する簡素な警告](https://www.fxsitecompat.dev/ja/docs/2016/insecure-password-input-warning-will-be-enabled-by-default/) が Firefox 51 より初期設定で有効化され、非 HTTPS ページ上で `<input type="password">` が見つかるたびにアドレスバー上に壊れた南京錠アイコンが表示されるようになりました。Firefox 52 ではこのセキュリティ対策がさらに進み、そうした安全でないログインフォームへの自動補完が無効化され、むしろ `<input>` 要素のすぐ下により目立つ [コンテキスト形式の警告メッセージ](https://developer.mozilla.org/docs/Web/Security/Insecure_passwords) が表示されるようになりました。

ウェブマスターの皆さんには、お客さんが安心して安全にログインできるよう、すべてのフォームを HTTPS ページへ移動するよう強く推奨します。まだご存じない方もいるかと思いますが、[Let's Encrypt](https://letsencrypt.org/) は信頼できる SSL/TLS 証明書を無料で発行しています。
