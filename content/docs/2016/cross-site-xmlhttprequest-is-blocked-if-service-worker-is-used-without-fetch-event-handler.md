---
title: "Cross-site `XMLHttpRequest` is blocked if Service Worker is used without `fetch` event handler"
date: "2016-02-07T22:27:00-05:00"
categories: ["dom", "networking"]
tags: []
versions: ["44"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1243453"
      title: "Bug 1243453 - Missing Origin header in Cross Origin Request resulting in Cross-Origin Request Blocked"
aliases:
    - "/en-CA/docs/2016/cross-site-xmlhttprequest-is-blocked-due-to-missing-origin-header/"
---
Firefox 44 has introduced a regression regarding `XMLHttpRequest` and Service Workers where [cross-site HTTP requests](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS) don't work properly when the site has a Service Worker and it's not handling the [`fetch` event](https://developer.mozilla.org/en-US/docs/Web/API/FetchEvent). When this issue occurs, the `Origin` header is missing in `GET` requests, resulting in an unnecessary preflight `OPTIONS` request and subsequent failed `GET` request. The bug has been fixed with Firefox 45. The workaround for Firefox 44 is adding a simple event listener to the worker code like this:

```js
self.addEventListener('fetch', function(event) {
  event.respondWith(fetch(event.request));
});
```

**Update**: Clarified the condition that involves the Service Worker API and added the workaround, according to the bug comments.
