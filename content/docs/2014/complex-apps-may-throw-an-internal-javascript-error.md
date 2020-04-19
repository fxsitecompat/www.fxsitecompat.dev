---
title: "Complex apps may throw an internal JavaScript error"
date: "2014-07-22T05:06:26-04:00"
categories: ["javascript"]
tags: []
releases: ["33"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083913"
      title: "Bug 1083913 – Switch statement too large internal error"
---
Complex Web appliations like WebGL-powered games may throw an internal JavaScript error that could not be found on the previous versions of Firefox. This regresson, caused by an improved source map support, will be fixed with Firefox 34.
