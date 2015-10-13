---
title: "`<frame>` や `<object>` 内のドキュメントは全画面表示をリクエストできなくなりました"
date: "2015-10-13T02:44:00-04:00"
categories: ["dom"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1212299": "Bug 1212299 - Forbid documents inside <frame> and <object> from requesting fullscreen"
---
Firefox は、`<frame>` や `<object>` 内のドキュメントによる [Fullscreen API](https://developer.mozilla.org/ja/docs/Web/API/Fullscreen_API) の使用を誤って許容していました。仕様に準拠するためこの挙動が修正され、最上位のドキュメントと `<iframe>` 内のドキュメントだけが全画面表示をリクエストできるようになりました。
