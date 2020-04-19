---
title: "CSP `referrer` ディレクティブが削除されました"
date: "2018-05-08T17:17:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["62", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1302449"
      title: "Bug 1302449 - deprecating the \"referrer\" directive in CSP"
---
[Firefox 52](https://www.fxsitecompat.dev/ja/docs/2017/csp-referrer-directive-has-been-deprecated/) 以降廃止予定となっていた Content Security Policy (CSP) [`referrer`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/referrer) ディレクティブが、[`Referrer-Policy`](https://developer.mozilla.org/docs/Web/HTTP/Headers/Referrer-Policy) HTTP に置き換えられる形で Firefox 62 で削除されました。2017 年 1 月公開の [Chrome 56](https://developers.google.com/web/updates/2016/12/chrome-56-deprecations) で既に対応が廃止されていることから、互換性リスクは低いはずです。
