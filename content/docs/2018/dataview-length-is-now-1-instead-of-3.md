---
title: "`DataView.length` is now `1` instead of `3`"
date: "2018-12-21T04:02:00-05:00"
categories: ["javascript"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1334813"
      title: "Bug 1334813 - Should DataView.length be 1 ?"
---
The `length` property on the [`DataView`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/DataView) constructor was previously `3` as per the ECMAScript 6 draft. Starting with Firefox 65, it will be `1` to follow the current spec. Some other browsers may still return `3` at this time.
