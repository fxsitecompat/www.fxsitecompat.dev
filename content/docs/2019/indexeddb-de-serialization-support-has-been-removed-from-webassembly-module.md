---
title: "IndexedDB de-serialization support has been removed from `WebAssembly.Module`"
date: "2019-08-13T16:15:00-04:00"
categories: ["misc"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1561876"
      title: "Bug 1561876 - Remove support for de-serializing WebAssembly.Modules in IDB"
---
Firefox 70 has removed the experimental IndexedDB de-serialization support for [`WebAssembly.Module`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WebAssembly/Module). The serialization support has already been removed with [Firefox 63](https://www.fxsitecompat.dev/en-CA/docs/2018/indexeddb-serialization-support-has-been-removed-from-webassembly-module/).
