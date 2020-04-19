---
title: "`FetchEvent.isReload` has been removed"
date: "2020-01-26T20:38:00-05:00"
categories: ["dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1264175"
      title: "Bug 1264175 - Remove FetchEvent.isReload"
---
The [`isReload`](https://developer.mozilla.org/docs/Web/API/FetchEvent/isReload) property on the `FetchEvent` interface has been removed with Firefox 74 because it was dropped from the Service Workers spec back in 2017. You can instead use the [`cache`](https://developer.mozilla.org/docs/Web/API/Request/cache) property on the `Request` interface and check if the value is `reload`.

```js
// Don’t do this
if (event.isReload) { ... }
// Do this
if (event.request.cache === 'reload') { ... }
```
