---
title: "`window` no longer accepts indexed custom properties"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=828787"
      title: "Bug 828787 – Stop allowing indexed expandos on windows"
---
Setting indexed expandos (custom properties which have number as the property name) on the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/window) object is no longer allowed. Your code like `window[2] = "myString"` will be ignored from now on.
