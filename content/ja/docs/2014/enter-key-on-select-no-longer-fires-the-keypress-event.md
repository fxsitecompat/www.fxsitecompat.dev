---
title: "`<select>` 上で Enter キーを押しても `keypress` イベントは呼び出されなくなりました"
date: "2014-02-07T11:57:09-05:00"
categories: [event-handling]
tags: []
versions: ["29"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=935876": "Bug 935876 – <select> element shouldn\'t consume key events which don\'t cause any default action"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1008244": "Bug 1008244 – Regression in 29: \"Enter\" key on <select> element no longer fires a keypress event"
---
`multiple` 属性が付かない [`<select>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/select) 要素は、意図しないフォーム送信を防ぐため、<kbd>Enter</kbd> キーが押されたときに [`keypress`](https://developer.mozilla.org/ja/docs/Web/Reference/Events/keypress) イベントを呼び出さなくなりました。開発者は代わりに [`keydown`](https://developer.mozilla.org/ja/docs/Web/Reference/Events/keydown) イベントを監視することで同じことができます。
