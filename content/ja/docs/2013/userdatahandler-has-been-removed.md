---
title: "`UserDataHandler` が削除されました"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=910751"
      title: "Bug 910751 – Hide UserDataHandler from content"
---
廃止予定となっていた [`UserDataHandler`](https://developer.mozilla.org/ja/docs/Web/API/UserDataHandler) インタフェースが削除されました。[`Node.setUserData`](https://developer.mozilla.org/ja/docs/Web/API/Node.setUserData)、[`Node.getUserData`](https://developer.mozilla.org/ja/docs/Web/API/Node.getUserData) 両メソッドは [Firefox 22 で既に削除されています](https://www.fxsitecompat.com/ja/docs/2013/node-getuserdata-and-setuserdata-have-been-removed/)。
