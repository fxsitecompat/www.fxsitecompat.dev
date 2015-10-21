---
title: "`navigator.mozKeyboard` が削除されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=986992": "Bug 986992 – Remove navigator.mozKeyboard"
---
[Firefox 16](https://developer.mozilla.org/ja/Mozilla/Firefox/Releases/16) 以降実装されている [Firefox OS](https://developer.mozilla.org/ja/Firefox_OS) 向けの [`navigator.mozKeyboard`](https://developer.mozilla.org/ja/docs/Web/API/navigator.mozKeyboard) が削除されました。`removeFocus`、`setSelectedOption`、`setSelectedOptions`、`setValue` メソッドは [`navigator.mozInputMethod`](https://developer.mozilla.org/ja/docs/Web/API/navigator.mozInputMethod) へ移されました。
