---
title: "Setting `document.domain` in a sandboxed `iframe` is no longer allowed"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
versions: ["26"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=907892"
      title: "Bug 907892 – Disallow setting document.domain in sandboxed iframes"
---
Trying to set the [`document.domain`](https://developer.mozilla.org/docs/Web/API/document.domain) property on a page embedded in an [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) with the `sandbox` attribute will throw a security error from now on.
