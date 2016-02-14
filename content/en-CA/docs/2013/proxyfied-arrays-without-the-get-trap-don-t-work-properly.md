---
title: "Proxyfied arrays without the `get` trap don\'t work properly"
date: "2013-02-06T08:44:10-05:00"
categories: ["javascript"]
tags: []
versions: ["21"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=895223": "Bug 895223 – Can\'t JSON stringify a proxy to an array"
---
The [`Proxy`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) object allows developers to *proxyfy* an object. All traps in the handler are optional, but starting with Firefox 21, proxyfied arrays without the `get` trap are not working properly. If the `get` trap is not defined, [`Array.length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length) returns `0` and the `set` trap doesn't get called. A workaround is to add the no-op `get` trap even if it's not necessary in your code.

**Update**: This issue has been fixed with Firefox 40.
