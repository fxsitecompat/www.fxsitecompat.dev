---
title: "Synchronous `XMLHttpRequest` has been deprecated"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=969671": "Bug 969671 – Warn about use of sync XHR in the main thread"
---
The `async` argument of the [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) constructor is `true` by default, and `false` makes the request synchronous. Developers now get an warning in the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) if a [synchronous request](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Synchronous_and_Asynchronous_Requests#Synchronous_request) is used on the main thread, or the outside of [workers](https://developer.mozilla.org/en-US/docs/Web/Guide/Performance/Using_web_workers), since it's now considered deprecated due to the negative effects to the user experience.

Possible solutions: using synchronous requests in a [`Worker`](https://developer.mozilla.org/en-US/docs/Web/API/Worker), or using asynchronous requests in a [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise).
