---
title: "Constants of some IndexedDB-related interfaces have been removed"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
releases: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=887524"
      title: "Bug 887524 – Move IDBRequest to WebIDL"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=888598"
      title: "Bug 888598 – Move IDBTransaction to WebIDL"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=891944"
      title: "Bug 891944 – Move IDBCursor to WebIDL"
---
The following constants on the [`IDBRequest`](https://developer.mozilla.org/docs/Web/API/IDBRequest), [`IDBTransaction`](https://developer.mozilla.org/docs/Web/API/IDBTransaction) and [`IDBCursor`](https://developer.mozilla.org/docs/Web/API/IDBCursor) interfaces have been removed due to the removal from the spec: `IDBRequest.LOADING`, `IDBRequest.DONE`, `IDBTransaction.READ_ONLY`, `IDBTransaction.READ_WRITE`, `IDBTransaction.VERSION_CHANGE`, `IDBCursor.NEXT`, `IDBCursor.NEXT_NO_DUPLICATE`, `IDBCursor.PREV` and `IDBCursor.PREV_NO_DUPLICATE`.
