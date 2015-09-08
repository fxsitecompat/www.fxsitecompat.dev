---
title: "`document.referrer` implementation has been updated for the latest spec"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
versions: "19"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=809290": "Bug 809290 – document.referrer should be based on the script entry point"
---
When the URL of a nested inline frame ([`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe)) or a grandchild window is programmatically changed from the parent window, the value of the [`document.referrer`](https://developer.mozilla.org/en-US/docs/Web/API/document.referrer) property now points the URL of the parent window where the script is written instead of the child window that refers directly. This is due to a change of the spec and leads to the same behavior as Internet Explorer and Opera. WebKit to follow.
