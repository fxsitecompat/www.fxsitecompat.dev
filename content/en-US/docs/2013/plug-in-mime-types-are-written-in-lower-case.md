---
title: "Plug-in MIME types are written in lower-case"
date: "2013-12-09T02:32:17-05:00"
categories: ["dom", "plugins"]
tags: []
versions: "28"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=206659": "Bug 206659 - Plugin not found, because MIME type has upper-case letters"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=985859": "Bug 985859 - navigator.mimeTypes has lower-cased MIME types since Firefox 28 while preserving case on earlier versions"
---
In Firefox 28, MIME types exposed in the [`document.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/document.plugins), [`window.navigator.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/window.navigator.plugins) and [`window.navigator.mimeTypes`](https://developer.mozilla.org/en-US/docs/Web/API/window.navigator.mimeTypes) properties are designated by lower-case letters, instead of the original mixed-case or upper-case type. This has been considered as a regression and fixed in Firefox 29. A workaround: use the [`String.toLowerCase`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase) method when you try to find a specific MIME type.
