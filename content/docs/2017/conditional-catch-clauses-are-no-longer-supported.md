---
title: "Conditional `catch` clauses are no longer supported"
date: "2017-11-15T11:49:00-05:00"
categories: ["javascript"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1228841"
      title: "Bug 1228841 - Remove support for conditional catch expressions"
aliases:
    - "/en-CA/docs/2015/conditional-catch-clause-support-will-be-removed/"
---
The support for non-standard [conditional `catch` clauses](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch#Conditional_catch_clauses) has been removed with Firefox 59. Use the standard [`if...else`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statement instead, as explained in the MDN document. Because it has never been implemented by any other browsers, the compatibility risk should be very low.
