---
title: "`Response`'s default `statusText` has become empty string"
date: "2019-05-13T04:32:00-04:00"
categories: ["dom", "networking"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1508996"
      title: "Bug 1508996 - Change Response's statusText's default"
---
On Firefox 67 and later, the default value of the [`Response.statusText`](https://developer.mozilla.org/docs/Web/API/Response/statusText) property will be an empty string. It was previously `"OK"`. If you just want to check if the request was successful, it's better to use the boolean [`ok`](https://developer.mozilla.org/docs/Web/API/Response/ok) property instead.
