---
title: "Network error for async XHR now fires `error` event instead of throwing, `getAllResponseHeaders` will be empty"
date: "2016-08-01T00:04:00-04:00"
categories: ["dom"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=709991"
      title: "Bug 709991 - [XHR2] Cross-origin XHR with username/password in URL throws"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1286744"
      title: "Bug 1286744 - [XHR2] GetAllResponseHeaders() should return an empty string if the XHR failed."
aliases:
    - "/docs/2016/network-error-for-async-xhr-now-fires-error-event-instead-of-throwing/"
---
Previously, Firefox was throwing a `NetworkError` exception when detecting a network error for asynchronous [`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest). On Firefox 50 and later, the browser instead fires an [`error`](https://developer.mozilla.org/en-US/docs/Web/Events/error) event asynchronously in the same fashion as [loading cross-origin worker firing an `error` event](https://www.fxsitecompat.com/en-CA/docs/2016/loading-cross-origin-worker-now-fires-error-event-instead-of-throwing-worker-in-sandboxed-iframe-no-longer-allowed/) since Firefox 45. Use an [`onerror`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequestEventTarget/onerror) handler in conjunction with a [`try-catch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch) statement to gently handle both cases:

```js
var xhr = new XMLHttpRequest();
xhr.addEventListener('load', function (event) {
  // ...
});
xhr.addEventListener('error', function (event) {
  // Handle a network error for newer browsers
});
xhr.open('GET', url, true);
try {
  xhr.send(null);
} catch (ex) {
  // Handle a network error for older browsers
}
```

Note that synchronous `XMLHttpRequest` will continue throwing an exception.

In a related development, the [`XMLHttpRequest.getAllResponseHeaders`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/getAllResponseHeaders) method now returns an empty string when a network error occurred.
