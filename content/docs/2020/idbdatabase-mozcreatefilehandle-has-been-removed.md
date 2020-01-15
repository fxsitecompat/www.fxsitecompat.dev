---
title: "`IDBDatabase.mozCreateFileHandle()` has been removed"
date: "2020-01-14T21:26:00-05:00"
categories: ["dom"]
tags: []
versions: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1024312"
      title: "Bug 1024312 - Deprecate mozCreateFileHandle() in favor of createMutableFile()"
---
The non-standard `mozCreateFileHandle` method on the [`IDBDatabase`](https://developer.mozilla.org/docs/Web/API/IDBDatabase) interface, deprecated since [Firefox 33](https://www.fxsitecompat.dev/en-CA/docs/2014/filehandle-api-has-been-updated/), has been removed with Firefox 74. Use the standard `createMutableFile` method instead.
