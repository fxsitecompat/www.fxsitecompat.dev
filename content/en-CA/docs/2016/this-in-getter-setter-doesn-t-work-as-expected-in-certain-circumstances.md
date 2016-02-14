---
title: "`this` in getter/setter doesn't work as expected in certain circumstances"
date: "2016-01-02T12:42:00-05:00"
categories: ["javascript"]
tags: []
versions: ["41"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1232269": "Bug 1232269 - Getter or setter on unboxed expando object is called with the expando as |this|"
---
Firefox 41 has introduced a regression where the [`this` keyword in a getter or setter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this#this_with_a_getter_or_setter) cannot refer the relevant object under certain circumstances, leading to an unexpected `TypeError` while accessing the property. In the bug reporter's case, the issue occurred with an object containing a large array, but it may happen in other conditions according to Mozilla developers. The issue has been fixed with Firefox 45.
