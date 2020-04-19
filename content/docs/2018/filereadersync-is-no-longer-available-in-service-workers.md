---
title: "`FileReaderSync` is no longer available in service workers"
date: "2018-05-08T19:17:00-04:00"
categories: ["dom"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1405552"
      title: "Bug 1405552 - Do not expose FileReaderSync to serviceworkers, to match the spec."
---
Starting with Firefox 61, the [`FileReaderSync`](https://developer.mozilla.org/docs/Web/API/FileReaderSync) API will be available only in dedicated and shared workers, not in service workers, according to the current File API spec. The asynchronous [`FileReader`](https://developer.mozilla.org/docs/Web/API/FileReader) API can be used instead.
