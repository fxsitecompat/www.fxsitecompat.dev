---
title: "`<meta http-equiv>` による Cookie の設定が許可されなくなります"
date: "2018-06-05T11:29:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457503"
      title: "Bug 1457503 - Remove <meta http-equiv=set-cookie> support"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AV_jwxqWdd0/discussion"
      title: "Intent to unship http-equiv cookies"
---
HTML [`<meta>`](https://developer.mozilla.org/docs/Web/HTML/Element/meta) 要素は、その `http-equiv` 属性を通じて、特定の HTTP レスポンスヘッダーを送信するのと同等の機能を提供しており、これを使って新たな Cookie を設定したり既存の Cookie を上書きしたりすることも可能です。

```html
<meta http-equiv="Set-Cookie" content="key=value">
```

クロスサイトスクリプティング (XSS) 攻撃のリスクを軽減するための努力の一環として、この古い挙動は最新の HTML 仕様から削除されました。[Google Chrome 65](https://bugs.chromium.org/p/chromium/issues/detail?id=767813) は既に 2018 年 3 月時点で対応を廃止しており、Firefox もまもなく続く見込みです。

ウェブ開発者には、標準の [`Set-Cookie`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) HTTP ヘッダーを `HttpOnly`、`Secure`、`SameSite` ディレクティブとともに用いることでセキュリティを高めることを推奨します。
