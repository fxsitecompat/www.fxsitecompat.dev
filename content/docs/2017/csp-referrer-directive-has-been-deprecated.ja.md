---
title: "CSP `referrer` ディレクティブが廃止予定となりました"
date: "2017-03-10T16:09:00-05:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1303682"
      title: "Bug 1303682 - Add deprecation warning before removing 'referrer' directive from CSP"
---
[`Referer`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Referer) HTTP ヘッダーの挙動を定義するために使われていた Content Security Policy (CSP) の [`referrer`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/referrer) ディレクティブが廃止予定となり、近く削除されることとなりました。今年 1 月公開の [Chrome 56](https://developers.google.com/web/updates/2016/12/chrome-56-deprecations) からは既に削除されています。代わりに [`Referrer-Policy`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Referrer-Policy) HTTP ヘッダーを使用してください。

**更新**: このディレクティブは [Firefox 62](https://www.fxsitecompat.dev/ja/docs/2018/csp-referrer-directive-has-been-removed/) で削除されました。
