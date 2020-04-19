---
title: "`<meta http-equiv>` による Cookie の設定が許可されなくなりました"
date: "2019-05-28T00:20:00-04:00"
categories: ["html", "privacy-security"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457503"
      title: "Bug 1457503 - Remove <meta http-equiv=set-cookie> support"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AV_jwxqWdd0/discussion"
      title: "Intent to unship http-equiv cookies"
aliases:
    - "/ja/docs/2018/setting-cookies-with-meta-http-equiv-will-no-longer-be-allowed/"
---
HTML `<meta>` 要素は、その `http-equiv` 属性を通じて、特定の HTTP レスポンスヘッダーを送信するのと同等の機能を提供しており、これを使って新たな Cookie を設定したり既存の Cookie を上書きしたりすることも可能です。

```html
<meta http-equiv="Set-Cookie" content="key=value">
```

クロスサイトスクリプティング (XSS) 攻撃のリスクを軽減するための努力の一環として、この古い挙動は最新の HTML 仕様と Firefox 68 から削除されました。[Google Chrome 65](https://www.chromestatus.com/feature/6170540112871424) は既に 2018 年 3 月時点で対応を廃止しています。

ウェブ開発者には、標準の [`Set-Cookie`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) HTTP ヘッダーを `HttpOnly`、`Secure`、`SameSite` ディレクティブとともに用いることでセキュリティを高めることを推奨します。
