---
title: "Service Workers `ExtendableEvent.waitUntil` implementation has been updated"
date: "2015-09-25T00:21:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1189644": "Bug 1189644 - \"Harness status: Timeout\" when running \"extendable-event-waituntil.https.html\" test"
---
The [`ExtendableEvent.waitUntil`](https://developer.mozilla.org/en-US/docs/Web/API/ExtendableEvent/waitUntil) method will throw an `InvalidStateError` if it's called outside the `ExtendableEvent` handler, as per the spec. Also, the `waitUntil` method now accepts multiple calls and the resulting [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)s will be concatenated in an array like [`Promise.all`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all).
