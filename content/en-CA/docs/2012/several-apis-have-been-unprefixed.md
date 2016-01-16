---
title: "Several APIs have been unprefixed"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=726378": "Bug 726378 – Unprefix IndexedDB"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=769571": "Bug 769571 – Unprefix battery and vibrator APIs"
---
The [IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) API has been unprefixed. Now you can use the standard [`indexedDB`](https://developer.mozilla.org/en-US/docs/Web/API/IDBEnvironment/indexedDB) property instead of `mozIndexedDB`. The [Battery Status](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API) and [Vibration](https://developer.mozilla.org/en-US/docs/Web/API/Vibration_API) APIs have also been unprefixed.
