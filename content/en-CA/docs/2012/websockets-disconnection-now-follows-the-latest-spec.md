---
title: "WebSockets disconnection now follows the latest spec"
date: "2012-10-09T06:00:00-04:00"
categories: ["networking"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=695636"
      title: "Bug 695636 - Update close steps to adhere to WS spec."
---
The [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API) implementation has been updated for the latest spec so the `error` or `close` event will no longer be fired while disconnecting due to the `close` method called in code.
