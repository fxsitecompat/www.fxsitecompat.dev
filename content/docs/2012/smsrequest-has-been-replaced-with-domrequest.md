---
title: "`SmsRequest` has been replaced with `DOMRequest`"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=760011"
      title: "Bug 760011 – Make nsIMozSmsRequest inherit from nsIDOMDOMRequest"
---
The `SmsRequest` object has been replaced with the [`DOMRequest`](https://developer.mozilla.org/docs/Web/API/DOMRequest) object that is more general and offers the same attributes and event handlers.
