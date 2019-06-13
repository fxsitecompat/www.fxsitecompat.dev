---
title: "`storage` option for `indexedDB.open()` has been removed"
date: "2018-06-03T23:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1354500"
      title: "Bug 1354500 - Remove the proprietary persistent indexedDB permission"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1451486"
      title: "Bug 1451486 - Add a pref for ignoring the storage attribute for indexedDB.open()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3b700_oeAzo/discussion"
      title: "Intent to unship: \"storage\" attribute in options for indexedDB.open()"
---
The non-standard `storage` option for the [`indexedDB.open`](https://developer.mozilla.org/docs/Web/API/IDBFactory/open) method, [deprecated since Firefox 60](https://www.fxsitecompat.dev/en-CA/docs/2018/storage-option-for-indexeddb-open-has-been-deprecated/), has been disabled by default with Firefox 62. Use the standardized Storage API's [`navigator.storage.persist`](https://developer.mozilla.org/docs/Web/API/StorageManager/persist) method instead. Given that the option has been implemented only in Firefox, the compatibility risk should be very low.
