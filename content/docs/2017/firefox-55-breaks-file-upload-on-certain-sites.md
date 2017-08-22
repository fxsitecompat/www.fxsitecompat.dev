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
---
Firefox 55 has introduced a regression where uploading a file from web forms doesn't work in certain circumstances due to a change in how upload stream is handled, likely leading to a 400 Bad Request error response from the server. Users are reporting that they cannot upload video thumbnails on *YouTube* which is offering an Ajaxy form, but static forms may also be affected. Mozilla developers are working on the solution.
