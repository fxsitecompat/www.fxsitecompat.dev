---
title: "`navigator.mozKeyboard` has been removed"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: ["31", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=986992"
      title: "Bug 986992 – Remove navigator.mozKeyboard"
---
`Navigator.mozKeyboard`, and its interface Keyboard, for [Firefox OS](https://developer.mozilla.org/Firefox_OS), implemented since [Firefox 16](https://developer.mozilla.org/Firefox/Releases/16), has been removed. The `removeFocus`, `setSelectedOption`, `setSelectedOptions` and `setValue` methods have been moved to [`navigator.mozInputMethod`](https://developer.mozilla.org/docs/Web/API/navigator/mozInputMethod).
