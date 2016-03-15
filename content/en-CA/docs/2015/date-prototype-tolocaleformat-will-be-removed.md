---
title: "`Date.prototype.toLocaleFormat` will be removed"
date: "2015-10-26T00:39:00-07:00"
categories: ["javascript"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818634"
      title: "Bug 818634 - Remove support for Date.prototype.toLocaleFormat"
---
The support for the [`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) method will be removed because it has not been standardized. ECMAScript 2015 (ES6) instead offers the [`toLocaleDateString`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) method that can be used to format dates easily in various languages.
