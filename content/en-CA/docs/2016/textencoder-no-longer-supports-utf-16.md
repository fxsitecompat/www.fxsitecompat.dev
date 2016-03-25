---
title: "`TextEncoder` no longer supports UTF-16"
date: "2016-03-25T18:52:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1257877"
      title: "Bug 1257877 - Remove support for UTF-16 from TextEncoder"
---
The support for the legacy `utf-16be` and `utf-16le` encodings has been removed from the [`TextDecoder`](https://developer.mozilla.org/en-US/docs/Web/API/TextDecoder) interface. Use `utf-8` instead.
