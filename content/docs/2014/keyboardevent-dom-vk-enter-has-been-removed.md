---
title: "`KeyboardEvent.DOM_VK_ENTER` has been removed"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=969247"
      title: "Bug 969247 – Get rid of related code of NS_VK_ENTER and nsIDOMKeyEvent::DOM_VK_ENTER"
---
The `DOM_VK_ENTER` constant has been removed from the [`KeyboardEvent`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent) interface and it now returns `null` instead of `14`. This should not break any existing code since it has never used in key events like [`keydown`](https://developer.mozilla.org/docs/Web/Events/keydown) or [`keypress`](https://developer.mozilla.org/docs/Web/Events/keypress), but you may want to remove it if you have. The `DOM_VK_RETURN` constant represents both <kbd>Enter</kbd> and <kbd>Return</kbd> keys.
