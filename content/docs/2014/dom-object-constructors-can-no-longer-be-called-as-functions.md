---
title: "DOM object constructors can no longer be called as functions"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
releases: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=916644"
      title: "Bug 916644 – Disallow calling WebIDL constructors as functions on the web"
---
Previously, [WebIDL](https://dxr.mozilla.org/mozilla-central/source/dom/webidl/) constructors could be called without the [`new`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/new) operator. Starting with Firefox 30, such code will raise a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError) like Chrome and Safari. For example, `var req = XMLHttpRequest();` should be `var req = new XMLHttpRequest();`.
