---
title: "`DOMError` has been removed in favour of `DOMException`"
date: "2017-10-03T04:30:00-04:00"
categories: ["dom"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120178"
      title: "Bug 1120178 - Remove DOMError"
---
The [`DOMError`](https://developer.mozilla.org/en-US/docs/Web/API/DOMError) interface has been removed with Firefox 58 because it's no longer standardized in the DOM4 spec. From now on, the `error` property on [`FileReader`](https://developer.mozilla.org/en-US/docs/Web/API/FileReader), [`IDBRequest`](https://developer.mozilla.org/en-US/docs/Web/API/IDBRequest), [`IDBTransaction`](https://developer.mozilla.org/en-US/docs/Web/API/IDBTransaction) and [`RTCPeerConnection`](https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection) objects will return a [`DOMException`](https://developer.mozilla.org/en-US/docs/Web/API/DOMException) instead. This change should not affect your code unless it checks for the object type for some reason, like below:

```js
error instanceof DOMError
```
