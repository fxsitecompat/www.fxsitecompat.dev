---
title: "`online`/`offline` events are no longer fired on `document` and `document.body`"
date: "2018-05-08T18:25:00-04:00"
categories: ["dom", "html"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1457166"
      title: "Bug 1457166 - Figure out what's the right target of the online / offline events."
---
Previously, [`online` and `offline` events](https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events) were fired on `document.body` and bubbled up to `document` and `window`, which was wrong according to the current HTML spec. Firefox 61 has fixed the non-standard behaviour so those events will be fired only on `window`. Note that the `ononline` and `onoffline` attributes on the `<body>` element are valid and therefore still available.

```js
// Don't do this
document.body.addEventListener('online', ...);
document.body.addEventListener('offline', ...);
document.addEventListener('online', ...);
document.addEventListener('offline', ...);

// Do this
window.addEventListener('online', ...);
window.addEventListener('offline', ...);
```
