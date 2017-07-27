---
title: "Prefixed `XMLHttpRequest` response types will be removed"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120171"
      title: "Bug 1120171 - Remove support for moz-prefixed XHR responseTypes"
---
A couple of non-standard, `moz`-prefixed values returned by the [`XMLHttpRequest.responseType`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest#xmlhttprequest-responsetype) property, including `moz-blob`, `moz-chunked-text` and `moz-chunked-arraybuffer`, are considered to be removed.
