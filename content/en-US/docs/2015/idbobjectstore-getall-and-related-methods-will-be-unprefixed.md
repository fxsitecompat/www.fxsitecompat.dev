---
title: "`IDBObjectStore.getAll` and related methods will be unprefixed"
date: "2015-10-25T21:09:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=920633": "Bug 920633 - Add getAllKeys to IDBObjectStore"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1196841": "Bug 1196841 - Add EnforceRange to getAll/getAllKeys to match the spec, and expose them unconditionally"
    "https://groups.google.com/d/topic/mozilla.dev.platform/De8vLz23Yao/discussion": "Intent to ship: IDB getAll/getAllKeys/openKeyCursor"
---
The `IDBObjectStore.mozGetAll`, `IDBIndex.mozGetAll` and `IDBIndex.mozGetAllKeys` methods will be unprefixed in the near future. Those unprefixed versions, `IDBObjectStore.getAll`, `IDBIndex.getAll` and `IDBIndex.getAllKeys`, have actually been implemented with Firefox 27 but disabled by default.
