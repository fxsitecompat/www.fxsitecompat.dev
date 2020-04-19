---
title: "`src` が空の `<img>` が `error` イベントを発生させます"
date: "2016-09-15T22:39:00-04:00"
categories: ["dom"]
tags: []
versions: ["51", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=599975"
      title: "Bug 599975 - Fire \"error\" event when img src is null or empty"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1308069"
      title: "Bug 1308069 - Bing maps is incompletely updated."
---
Firefox 51 以降、現行の HTML 仕様に従い、`src` 属性が空だった場合に `<img>` 要素が [`error`](https://developer.mozilla.org/docs/Web/Events/error) イベントを発生させます。このイベントは、`src` DOM プロパティの値が空文字列や `null` へ動的に変更された場合にも発生します。

**更新**: *Bing マップ* がこの変更により正しく動作していません。
