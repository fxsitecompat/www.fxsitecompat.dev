---
title: "`console` will be overridden by a global variable with the same name"
date: "2014-03-21T04:50:04-04:00"
categories: ["javascript"]
tags: []
versions: "30"
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=965860": "Bug 965860 – Rewrite ConsoleAPI in C++"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1024806": "Bug 1024806 – Ro.me does not load after clicking the try anyway warning. Worked in ff29."
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1024899": "Bug 1024899 – After update from v 29.0.1 to v 30.0 the site: https://home.cgm-life.de/fb363286-e393-4a31-84c1-9c60e07c6cef cannot be reached (responsive design - twitter bootstrap - Angular JS)"
---
Due to the new implementation of the [`console`](https://developer.mozilla.org/en-US/docs/Web/API/console) object, it will be overridden by a user-defined global variable named `console` if exists, leading to unexpected behavior. At least 2 sites are known to be broken where `var console` is defined at the top level code and [`console.log`](https://developer.mozilla.org/en-US/docs/Web/API/console.log) is subsequently called. Firefox 31 and above are not affected by this issue thanks to another implementation change.
