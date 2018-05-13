---
title: "`XMLHttpRequest` now sends HTML document as `text/html` instead of `application/xml`"
date: "2015-10-23T02:04:00-07:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=918771"
      title: "Bug 918771 - XMLHttpRequest (XHR) send() of an HTML document sends it as application/xml, not text/html"
---
Previously, the [`XMLHttpRequest.send`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest#send%28%29) method of Firefox was transmitting HTML documents as the `application/xml` MIME Type and adding an XML declaration `<?xml version="1.0"?>` to the documents. In order to improve interoperability, the XMLHttpRequest spec and Firefox implementation have been updated so HTML documents are now sent as `text/html` in the UTF-8 character encoding.
