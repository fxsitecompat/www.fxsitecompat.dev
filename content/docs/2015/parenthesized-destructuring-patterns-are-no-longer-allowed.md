---
title: "Parenthesized destructuring patterns are no longer allowed"
date: "2015-06-13T15:20:46-04:00"
categories: ["javascript"]
tags: []
releases: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1146136"
      title: "Bug 1146136 - Parenthesized AssignmentPatterns are not a valid LHS"
---
As part of the ES6 specification compliance, parenthesized destructuring patterns, like `([a, b]) = [1, 2]` or `({a, b}) = { a: 1, b: 2 }`, are now considered invalid and will throw a [`SyntaxError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError). See [Jeff Walden's blog post](https://whereswalden.com/2015/06/20/new-changes-to-make-spidermonkeys-and-firefoxs-parsing-of-destructuring-patterns-more-spec-compliant/) for details.
