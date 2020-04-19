---
title: "`MozConnection` interface is no longer a global object"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
releases: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=960945"
      title: "Bug 960945 – MozConnection should be NoInterfaceObject"
---
The [`Connection`](https://developer.mozilla.org/docs/Web/API/Connection) interface, currently prefixed as `MozConnection`, is no longer available on [`window`](https://developer.mozilla.org/docs/Web/API/window) as a global object. Use [`navigator.mozConnection`](https://developer.mozilla.org/docs/Web/API/navigator.mozConnection) to utilize the [Network Information API](https://developer.mozilla.org/docs/Web/API/Network_Information_API).
