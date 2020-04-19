---
title: "`DOMError` has been replaced with `DOMException`"
date: "2017-10-03T04:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120178"
      title: "Bug 1120178 - Remove DOMError"
aliases:
    - "/en-CA/docs/2017/domerror-has-been-removed-in-favour-of-domexception/"
---
The [`DOMError`](https://developer.mozilla.org/docs/Web/API/DOMError) interface is no longer used for errors in Firefox 58 and later because it has been removed from the DOM4 spec. From now on, the `error` property on [`FileReader`](https://developer.mozilla.org/docs/Web/API/FileReader), [`IDBRequest`](https://developer.mozilla.org/docs/Web/API/IDBRequest), [`IDBTransaction`](https://developer.mozilla.org/docs/Web/API/IDBTransaction) and [`RTCPeerConnection`](https://developer.mozilla.org/docs/Web/API/RTCPeerConnection) objects will return a [`DOMException`](https://developer.mozilla.org/docs/Web/API/DOMException) instead. This change should not affect your code unless it checks for the object type for some reason, like below:

```js
error instanceof DOMError
```

**Update**: The `DOMError` interface had remained until [Firefox 69](https://www.fxsitecompat.dev/en-CA/docs/2019/domerror-has-been-completely-removed/) when it's completely removed. This note has been corrected to reflect the fact.
