---
title: "配信元が異なるリソースから HTTP 認証ダイアログを表示できなくなりました"
date: "2015-04-27T13:17:23-04:00"
categories: ["privacy-security"]
tags: []
versions: "40"
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=647010": "Bug 647010 - Only present HTTP authentication dialogs if it is the top-level document initiating the auth"
---
Firefox はこれまで、他のブラウザと同様に、[`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe)、[`<img>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/img)、[`<script>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/script)、[`XMLHttpRequest`](https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest)、CSS [`background-image`](https://developer.mozilla.org/ja/docs/Web/CSS/background-image) などあらゆるリソースが HTTP 401 ベーシック認証ダイアログを表示することを許容していました。しかしこの挙動は、攻撃者が第三者のサイトに任意のリソースを埋め込んだり挿入したりすることができた場合、ユーザの認証情報を盗み出すのに悪用される恐れがありました。Firefox 40 以降では、ページ自体と [同一配信元](https://developer.mozilla.org/ja/docs/Web/Security/Same-origin_policy) のリソースのみが認証ダイアログを表示できるようになり、サイト互換性の問題を軽減しつつそうした潜在的な攻撃を防ぐ措置が講じられています。

必要な場合、この新しい挙動は、以下のいずれかの値を取る隠し設定 `network.auth.allow-subresource-auth` で変更できます。

* `0` - サブリソースが HTTP 認証ダイアログを開くことを許可しない
* `1` (既定値) - サブリソースが HTTP 認証ダイアログを開くことを許可するが、配信元が異なるサブリソースには許可しない
* `2` - 配信元が異なるサブリソースにも認証を許可する

出典: [modules/libpref/init/all.js](https://dxr.mozilla.org/mozilla-central/source/modules/libpref/init/all.js)

**更新**: ユーザからのフィードバックを受けて、この変更は  Firefox 41 Beta、42 Developer Edition および 43 Nightly から [バックアウト](https://bugzilla.mozilla.org/show_bug.cgi?id=1197944) され、`network.auth.allow-subresource-auth` 設定の既定値は `2` に戻されました。Firefox 40 向けにも、[以前の挙動に戻す](https://bugzilla.mozilla.org/show_bug.cgi?id=1201065) 組み込みホットフィックスアドオンの自動更新が <time datetime="2015-09-04">9 月 4 日</time> 以降に配信されています。

**更新**: ホットフィックスアドオンとの競合を防ぐため、Firefox 41 で [設定名が変更され](https://bugzilla.mozilla.org/show_bug.cgi?id=1202421) `network.auth.subresource-http-auth-allow` になりました。取り得る値と既定値 (`2`) は変わりません。
