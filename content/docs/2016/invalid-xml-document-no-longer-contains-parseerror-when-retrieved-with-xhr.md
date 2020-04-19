---
title: "Invalid XML document no longer contains `<parseerror>` when retrieved with XHR"
date: "2016-08-30T04:24:00-04:00"
categories: ["dom"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=289714"
      title: "Bug 289714 - Loaded-as-data XML documents should not generate <parsererror>"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/T5XmMus-aM0/discussion"
      title: "Intent to ship: XMLHttpRequest parsing errors will yield a null document for web content, not one with a <parsererror> root."
---
When loading an invalid XML document, Firefox shows a yellow page with an XML Parsing Error message rendered within a `<parseerror>` node. Firefox 51 and later will return `null` for the [`XMLHttpRequest.responseXML`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest/responseXML) property instead of such a custom error document.

You should observe an exception saying "XML Parsing Error: not well-formed" instead of sniffing `responseXML` to validate a document. This error message was simply "not well-formed" on Firefox 50 and prior.
