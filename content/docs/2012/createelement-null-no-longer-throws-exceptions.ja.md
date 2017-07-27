---
title: "`createElement(null)` が例外を投げなくなりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=802562"
      title: "Bug 802562 – createElement(null) should work like createElement(\"null\")"
---
[`document.createElement`](https://developer.mozilla.org/ja/docs/DOM/document.createElement) メソッドの引数が `null` だった場合、従来は例外 `INVALID_CHARACTER_ERR` が投げられていました。この引数は文字列として扱われるべきとして、`document.createElement("null")` と同等にみなし、`HTMLUnknownElement` オブジェクトを返すようになりました。
