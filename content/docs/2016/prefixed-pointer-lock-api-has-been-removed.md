---
title: "Prefixed Pointer Lock API has been removed"
date: "2016-07-31T17:13:00-04:00"
categories: ["dom"]
tags: []
versions: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=991899"
      title: "Bug 991899 - Unprefix pointer lock"
---
The [Pointer Lock API](https://developer.mozilla.org/docs/Web/API/Pointer_Lock_API) has been unprefixed as the spec is now considered stable. This includes the [pointerLockElement](https://developer.mozilla.org/docs/Web/API/Document/pointerLockElement) property, the [requestPointerLock](https://developer.mozilla.org/docs/Web/API/Element/requestPointerLock) and [exitPointerLock](https://developer.mozilla.org/docs/Web/API/Document/exitPointerLock) methods, as well as the [pointerlockchange](https://developer.mozilla.org/docs/Web/Events/pointerlockchange) and [pointerlockerror](https://developer.mozilla.org/docs/Web/Events/pointerlockerror) events.

At the same time, the `moz`-prefixed API is disabled by default without a transition period. Given that Google Chrome has already removed the `webkit`-prefixed API support, Mozilla developers are not expecting any compatibility issues.
