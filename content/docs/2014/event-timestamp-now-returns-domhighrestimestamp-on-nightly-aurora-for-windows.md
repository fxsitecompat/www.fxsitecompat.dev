---
title: "`event.timeStamp` now returns `DOMHighResTimeStamp` on Nightly/Aurora for Windows"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
versions: ["33"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1022396"
      title: "Bug 1022396 – Make Event.timeStamp return a DOMHighResTimeStamp on Windows (was Event.timeStamp should be relative to 1st January 1970 rather than the system start)"
---
On the [Nightly](http://nightly.mozilla.org/) and [Aurora](http://aurora.mozilla.org/) channels for Windows, the [`event.timeStamp`](https://developer.mozilla.org/en-US/docs/Web/API/event.timeStamp) property now returns a [`DOMHighResTimeStamp`](https://developer.mozilla.org/en-US/docs/Web/API/DOMHighResTimeStamp) in microseconds, instead of a traditional time stamp in milliseconds. This feature is still disabled on the Beta and Release channels, and [not yet implemented on other platforms](https://bugzilla.mozilla.org/show_bug.cgi?id=1026803).
