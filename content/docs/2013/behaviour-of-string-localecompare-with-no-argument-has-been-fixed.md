---
title: "Behaviour of `String.localeCompare` with no argument has been fixed"
date: "2013-02-06T08:44:10-05:00"
categories: ["javascript"]
tags: []
versions: ["21"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=789393"
      title: "Bug 789393 – String.prototype.localeCompare() with no argument always returns 0"
aliases:
    - "/en-CA/docs/2013/behaviour-of-string-localecompare-with-no-argument-has-been-fixed/"
---
The [`String.localeCompare`](https://developer.mozilla.org/docs/JavaScript/Reference/Global_Objects/String/localeCompare) method implementation has been updated to conform to the latest ECMAScript 5 spec. If no argument is passed, the method takes the `"undefined"` string as the argument.
