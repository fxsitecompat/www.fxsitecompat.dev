---
title: "`IDBObjectStore.getAll` and related methods have been unprefixed"
date: "2015-10-25T21:09:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=920633": "Bug 920633 - Add getAllKeys to IDBObjectStore"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1196841": "Bug 1196841 - Add EnforceRange to getAll/getAllKeys to match the spec, and expose them unconditionally"
    "https://groups.google.com/d/topic/mozilla.dev.platform/De8vLz23Yao/discussion": "Intent to ship: IDB getAll/getAllKeys/openKeyCursor"
aliases:
    - "/docs/2015/idbobjectstore-getall-and-related-methods-will-be-unprefixed/"
---
The `IDBObjectStore.mozGetAll`, `IDBIndex.mozGetAll` and `IDBIndex.mozGetAllKeys` methods have been unprefixed with Firefox 44. Those unprefixed versions, `IDBObjectStore.getAll`, `IDBIndex.getAll` and `IDBIndex.getAllKeys`, implemented with Firefox 27 behind a hidden preference, are now enabled by default.
