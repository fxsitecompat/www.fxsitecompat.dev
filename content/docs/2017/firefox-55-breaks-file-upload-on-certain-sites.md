---
title: "Firefox 55 breaks file upload on certain sites"
date: "2017-08-22T13:24:00-04:00"
categories: ["dom"]
tags: []
versions: ["55"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1383518"
      title: "Bug 1383518 - Uploading thumbnails to YouTube, picture to Tweakers.net not working on Firefox 55+"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1393063"
      title: "Bug 1393063 - XHR send of FormData with certain Blobs hangs indefinitely (Firefox 55.0.0 - 55.0.2)"
---
Firefox 55 has introduced a regression where uploading a file from web forms doesn't work in certain circumstances due to a change in how upload stream is handled, likely leading to a 400 Bad Request error response from the server. Users are reporting that they cannot upload video thumbnails on *YouTube* which is offering an Ajaxy form, but static forms may also be affected. Mozilla developers are working on the solution.

**Update**: This regression, turned out to be a bug involving service workers, has been fixed with Firefox 55.0.3. However, there's another upload regression in Firefox 55 where async `XMLHttpRequest` or `fetch` using a [`FormData`](https://developer.mozilla.org/en-US/docs/Web/API/FormData) with certain `Blob`s will fail even without service workers. Mozilla developers are working on this bug as well.

**Update 2**: The `FormData` regression has been fixed with Firefox 56.
