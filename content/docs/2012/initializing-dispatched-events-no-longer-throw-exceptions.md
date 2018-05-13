---
title: "Initializing dispatched events no longer throw exceptions"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=768310"
      title: "Bug 768310 – initEvent on already-dispatched event should be a noop (rather than throwing)"
---
Previously, executing [`initEvent`](https://developer.mozilla.org/docs/Web/API/event.initEvent) on events dispatched with [`dispatchEvent`](https://developer.mozilla.org/docs/Web/API/EventTarget.dispatchEvent) thrown an exception. The behaviour has been changed to do nothing like the other browsers.
