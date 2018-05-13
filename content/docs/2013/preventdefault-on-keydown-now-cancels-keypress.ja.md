---
title: "`keydown` の `preventDefault` が `keypress` をキャンセルするようになりました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: ["25"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=501496"
      title: "Bug 501496 – preventDefault on keydown does not cancel following keypress"
---
従来、[`keydown`](https://developer.mozilla.org/docs/Web/Reference/Events/keydown) イベント上で [`preventDefault`](https://developer.mozilla.org/docs/Web/API/event.preventDefault) を呼び出しても、それに続く [`keypress`](https://developer.mozilla.org/docs/Web/Reference/Events/keypress) イベントはキャンセルされませんでした。これが DOM Level 3 Events (D3E) 仕様や他のブラウザーの挙動と一致するように修正されました。
