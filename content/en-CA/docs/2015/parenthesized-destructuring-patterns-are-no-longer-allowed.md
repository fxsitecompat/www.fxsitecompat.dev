---
title: "Parenthesized destructuring patterns are no longer allowed"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
versions: ["41"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1146136"
      title: "Bug 1146136 - Parenthesized AssignmentPatterns are not a valid LHS"
---
As part of the ES6 specification compliance, parenthesized destructuring patterns, like `([a, b]) = [1, 2]` or `({a, b}) = { a: 1, b: 2 }`, are now considered invalid and will throw a [`SyntaxError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError). See [Jeff Walden's blog post](http://whereswalden.com/2015/06/20/new-changes-to-make-spidermonkeys-and-firefoxs-parsing-of-destructuring-patterns-more-spec-compliant/) for details.
