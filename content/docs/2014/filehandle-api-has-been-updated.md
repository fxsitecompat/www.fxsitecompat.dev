---
title: "FileHandle API has been updated"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
releases: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1006485"
      title: "Bug 1006485 – FileHandle: Rename FileHandle to MutableFile and LockedFile to FileHandle"
---
The implementation of the [FileHandle API](https://developer.mozilla.org/docs/Web/API/File_Handle_API) has been updated. The [`IDBDatabase.mozCreateFileHandle`](https://developer.mozilla.org/docs/Web/API/IDBDatabase.mozCreateFileHandle) method has been renamed to [`IDBDatabase.createMutableFile`](https://developer.mozilla.org/docs/Web/API/IDBDatabase.createMutableFile). Also, the [`FileHandle`](https://developer.mozilla.org/docs/Web/API/FileHandle) and [`LockedFile`](https://developer.mozilla.org/docs/Web/API/LockedFile) interfaces have been respectively renamed to [`IDBMutableFile`](https://developer.mozilla.org/docs/Web/API/IDBMutableFile) and [`IDBFileHandle`](https://developer.mozilla.org/docs/Web/API/IDBFileHandle), though consumers don't have to check these object names.

**Update**: The `mozCreateFileHandle` method has been removed with [Firefox 74](https://www.fxsitecompat.dev/en-CA/docs/2020/idbdatabase-mozcreatefilehandle-has-been-removed/).
