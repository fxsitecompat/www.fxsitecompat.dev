---
title: "`__noSuchMethod__` is no longer supported"
date: "2015-09-22T09:37:00-04:00"
categories: ["javascript"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=683218": "Bug 683218 - can we remove __noSuchMethod__, use proxies instead?"
---
The support for the non-standard [`Object.prototype.__noSuchMethod__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/noSuchMethod) property, [deprecated since Firefox 39](https://www.fxsitecompat.com/en-CA/docs/2015/nosuchmethod-has-been-deprecated/), has been dropped with Firefox 44. The ECMAScript 2015 (ES6) [`Proxy`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) object can be used instead to implement such a catch-all mechanism.
