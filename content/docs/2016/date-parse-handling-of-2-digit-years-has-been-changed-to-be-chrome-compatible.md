---
title: "`Date.parse` handling of 2-digit years has been changed to be Chrome compatible"
date: "2016-05-28T02:47:00-04:00"
categories: ["javascript"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1265136"
      title: "Bug 1265136 - new Date(<mm/dd/yy>) behaves differently in Firefox vs Chrome/Safari"
---
Parsing of strings with the [`Date`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date) constructor and the [`Date.parse`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/parse) method is implementation dependent, and Firefox was handling 2-digit years in the same way as Internet Explorer. Firefox 49 has [modified the logic](https://hg.mozilla.org/mozilla-central/rev/138521110469) to be compatible with Google Chrome so that any 2-digit year less than or equal to `50` is now treated as a 21st century year. For example, `04/16/17`, previously parsed as April 16, 1917, will be April 16, 2017. In terms of interoperability, Web developers are encouraged to always use the ISO 8601 format like `2017-04-16`.
