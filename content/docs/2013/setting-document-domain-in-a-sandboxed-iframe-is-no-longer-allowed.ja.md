---
title: "サンドボックス化した `iframe` 内では `document.domain` の設定が許容されなくなりました"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=907892"
      title: "Bug 907892 – Disallow setting document.domain in sandboxed iframes"
---
`sandbox` 属性付きの [`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe) で埋め込まれたページの [`document.domain`](https://developer.mozilla.org/ja/docs/Web/API/document.domain) プロパティを設定しようとすると、今後はセキュリティエラーが投げられます。
