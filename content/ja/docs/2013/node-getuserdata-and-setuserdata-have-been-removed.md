---
title: "`Node.getUserData` と `setUserData` が削除されました"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: "22"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=842372": "Bug 842372 – Make getUserData and setUserData ChromeOnly"
---
[`Node.getUserData`](https://developer.mozilla.org/ja/docs/Web/API/Node.getUserData)、[`Node.setUserData`](https://developer.mozilla.org/ja/docs/Web/API/Node.setUserData) 両メソッドが Web コンテンツから使用できなくなりました。[`Element.dataset`](https://developer.mozilla.org/ja/docs/Web/API/Element.dataset) もしくは [`WeakMap`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) で代用してください。
