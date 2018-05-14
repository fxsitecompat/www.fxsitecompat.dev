---
title: "`Content-Disposition` header\'s `name` parameter is no longer supported"
date: "2012-12-03T03:54:45-05:00"
categories: ["misc"]
tags: []
versions: ["19"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=776339"
      title: "Bug 776339 – remove support of Content-Disposition \"name\" parameter"
---
The `name` parameter included in the HTTP `Content-Disposition` header used for file downloading is now ignored. This parameter is non-standard and supported only by Firefox and Google Chrome. From now, use the standard `filename` parameter instead.
