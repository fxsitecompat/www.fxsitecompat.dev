---
title: "SVG と XPath の例外が `DOMException` に統一されました"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=743888"
      title: "Bug 743888 – Replace SVGException and XPathException with DOMException"
---
例外の `SVGException` と `XPathException` は削除され、[`DOMException`](https://developer.mozilla.org/docs/Web/API/DOMException) に置き換えられました。
