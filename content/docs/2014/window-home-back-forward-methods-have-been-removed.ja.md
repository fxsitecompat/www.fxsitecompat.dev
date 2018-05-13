---
title: "`window.home`、`back`、`forward` メソッドが削除されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1012944"
      title: "Bug 1012944 – User login and account creation on deezer.com broken since Firefox 30.0b1, say home.display is not a function"
---
Nescape に由来する非標準の [`window.home`](https://developer.mozilla.org/docs/Web/API/window.home)、[`window.back`](https://developer.mozilla.org/docs/Web/API/window.back)、[`window.forward`](https://developer.mozilla.org/docs/Web/API/window.forward) メソッドが削除されました。[ブラウザー履歴を操作](https://developer.mozilla.org/docs/Web/Guide/API/DOM/Manipulating_the_browser_history) するには標準の [`history.back`](https://developer.mozilla.org/docs/Web/API/history.back)、[`history.forward`](https://developer.mozilla.org/docs/Web/API/history.forward) メソッドを使用できます。
