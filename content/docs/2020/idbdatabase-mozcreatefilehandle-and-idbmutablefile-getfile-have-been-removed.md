---
title: "`IDBDatabase.mozCreateFileHandle()` and `IDBMutableFile.getFile()` have been removed"
date: "2020-01-14T21:26:00-05:00"
categories: ["dom"]
tags: []
releases: ["74"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1024312"
      title: "Bug 1024312 - Deprecate mozCreateFileHandle() in favor of createMutableFile()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1607791"
      title: "Bug 1607791 - Get rid of IDBMutableFile.getFile()"
aliases:
  - "/en-CA/docs/2020/idbdatabase-mozcreatefilehandle-has-been-removed/"
---
In Firefox 74, 2 changes have been made to the [FileHandle API](https://developer.mozilla.org/docs/Web/API/File_Handle_API).

The non-standard `mozCreateFileHandle` method on the [`IDBDatabase`](https://developer.mozilla.org/docs/Web/API/IDBDatabase) interface, deprecated since [Firefox 33](https://www.fxsitecompat.dev/en-CA/docs/2014/filehandle-api-has-been-updated/), has been removed. Use the standard `createMutableFile` method instead.

The non-standard `getFile` method on the [`IDBMutableFile`](https://developer.mozilla.org/docs/Web/API/IDBMutableFile) interface has also been removed. Since no other browsers support this, the compatibility impact should be minimum. The interface itself, [previously](https://www.fxsitecompat.dev/en-CA/docs/2014/filehandle-api-has-been-updated/) called `FileHandle`, will be removed in the near future.
