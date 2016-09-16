---
title: "`<img>` with empty `src` will fire `error` event"
date: "2016-09-15T22:39:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=599975"
      title: "Bug 599975 - Fire \"error\" event when img src is null or empty"
---
On Firefox 51 and later, according to the current HTML spec, the `<img>` element fires an [`error`](https://developer.mozilla.org/en-US/docs/Web/Events/error) event when the `src` attribute was empty. The event will also be fired when the `src` DOM property is dynamically changed to an empty value or `null`.
