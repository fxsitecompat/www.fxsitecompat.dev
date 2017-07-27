---
title: "安全でないパスワード入力警告が初期設定で有効となりました"
date: "2016-12-03T14:54:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319119"
      title: "Bug 1319119 - Turn on Insecure Password Warning in Firefox Release"
aliases:
  - "/docs/2016/insecure-password-input-warning-will-be-enabled-by-default/"
---
[Firefox 46](https://www.fxsitecompat.com/ja/docs/2015/non-https-sites-containing-login-form-will-be-marked-insecure/) 以降、現在表示されているページに `<input type="password">` が含まれていて、なおかつ接続が安全でない場合、Firefox Nightly と Developer Edition はロケーションバーに壊れた南京錠アイコンを表示しています。この [安全でないパスワード入力警告](https://twitter.com/FxSiteCompat/status/779224374742249472) は Firefox 50 で早期ベータ版にも拡大されました。Firefox 51 では、リリース版も含めすべてのチャンネルにおいて初期設定で有効となりました。

このインジケーターは今のところそれほど目立つものではありませんが、現在進んでいる [安全でない HTTP 廃止](https://www.fxsitecompat.com/ja/docs/2015/insecure-http-will-be-deprecated/) の一環として、[コンテキスト内 UI の変更](https://www.fxsitecompat.com/ja/docs/2017/insecure-login-forms-now-disable-autofill-show-warning-beneath-input-control/) などさらなる警告の追加が予定されています。Web 開発者には、顧客保護の観点から、すべてのログインフォームを HTTPS ページへ移すか、理想的には今あるページ自体を HTTPS にするよう強く推奨します。

この変更は、同じく 2017 年 1 月に [同様の変更](https://blog.chromium.org/2016/09/moving-towards-more-secure-web.html) を行う Google Chrome 56 と足並みを揃える形で行われます。
