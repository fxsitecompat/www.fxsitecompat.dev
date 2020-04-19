---
title: "`TextEncoder` no longer supports UTF-16"
date: "2016-03-25T18:52:00-04:00"
categories: ["dom"]
tags: []
releases: ["48", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257877"
      title: "Bug 1257877 - Remove support for UTF-16 from TextEncoder"
---
The support for the UTF-16BE and UTF-16LE encodings has been removed from the [`TextEncoder`](https://developer.mozilla.org/docs/Web/API/TextEncoder) interface, according to the latest Encoding standard. The [constructor](https://developer.mozilla.org/docs/Web/API/TextEncoder/TextEncoder) now ignores the optional `utfLabel` argument and UTF-8 will always be used instead.
