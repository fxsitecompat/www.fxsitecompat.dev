---
title: "`UserDataHandler` has been removed"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: "26"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=910751": "Bug 910751 – Hide UserDataHandler from content"
---
The deprecated [`UserDataHandler`](https://developer.mozilla.org/en-US/docs/Web/API/UserDataHandler) interface has been removed. The [`Node.setUserData`](https://developer.mozilla.org/en-US/docs/Web/API/Node.setUserData) and [`Node.getUserData`](https://developer.mozilla.org/en-US/docs/Web/API/Node.getUserData) methods have already been removed with [Firefox 22](https://www.fxsitecompat.com/en-US/versions/22/).
