---
title: "`initCloseEvent` and `createEvent(\'CloseEvent\')` have been removed"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: ["41"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1161950"
      title: "Bug 1161950 - Remove support for createEvent(\"CloseEvent\") / initCloseEvent"
---
The `CloseEvent.initCloseEvent` method has been removed and the [`document.createEvent`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createEvent) method no longer supports the `CloseEvent` type. The [`CloseEvent`](https://developer.mozilla.org/en-US/docs/Web/API/CloseEvent/CloseEvent) constructor can be used instead from now on.
