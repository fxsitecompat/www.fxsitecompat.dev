---
title: "IndexedDB serialization support has been removed from `WebAssembly.Module`"
date: "2018-08-16T10:25:00-04:00"
categories: ["misc"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1469395"
      title: "Bug 1469395 - Remove WebAssembly.Module IndexedDB serialization support"
---
Firefox 63 has removed the experimental IndexedDB serialization support for [`WebAssembly.Module`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WebAssembly/Module) which allowed to [cache compiled WebAssembly modules in IndexedDB](https://dzone.com/articles/webassembly-caching-to-html5-indexeddb), according to the latest WebAssembly spec, after several concerns have been raised. Given that the functionality has been implemented only in Firefox and Microsoft Edge, the compatibility risk should be low. [Regular HTTP caching](https://developer.mozilla.org/docs/Web/HTTP/Caching) or [Cache API](https://developer.mozilla.org/docs/Web/API/Cache) can be used instead.
