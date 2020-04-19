---
title: "`navigator.mozKeyboard` が削除されました"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
releases: ["31", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=986992"
      title: "Bug 986992 – Remove navigator.mozKeyboard"
---
[Firefox 16](https://developer.mozilla.org/Mozilla/Firefox/Releases/16) 以降実装されている [Firefox OS](https://developer.mozilla.org/Firefox_OS) 向けの [`navigator.mozKeyboard`](https://developer.mozilla.org/docs/Web/API/navigator.mozKeyboard) が削除されました。`removeFocus`、`setSelectedOption`、`setSelectedOptions`、`setValue` メソッドは [`navigator.mozInputMethod`](https://developer.mozilla.org/docs/Web/API/navigator.mozInputMethod) へ移されました。
