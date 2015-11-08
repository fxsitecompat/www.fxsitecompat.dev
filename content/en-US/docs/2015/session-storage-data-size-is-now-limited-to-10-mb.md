---
title: "Session storage data size is now limited to 10 MB"
date: "2015-11-08T14:32:00-08:00"
categories: ["dom"]
tags: []
versions: ["45"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1216250": "Bug 1216250 - Limit amount of DOM Storage data stored by Session Restore"
---
The amount of data that can be stored with the [Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API), specifically with the [`window.sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage) property, is now limited to 10 MB per [origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin) to prevent potential browser crashes. If you need to store a large amount of data locally, consider using the async [IndexedDB API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) instead.
