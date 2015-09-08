---
title: "`ProgressEvent.initProgressEvent` has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
versions: "22"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=843489": "Bug 843489 – [Progress Events] Remove support for ProgressEvent.initProgressEvent() and Document.createEvent(\"ProgressEvent\")"
---
The [`ProgressEvent.initProgressEvent`](https://developer.mozilla.org/en-US/docs/Web/API/ProgressEvent.initProgressEvent) method is no longer available, due to the removal from the spec. The support for `document.createEvent("ProgressEvent")` has also been dropped.
