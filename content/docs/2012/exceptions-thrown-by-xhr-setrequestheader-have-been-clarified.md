---
title: "Exceptions thrown by `XHR.setRequestHeader()` have been clarified"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=600111"
      title: "Bug 600111 – XMLHttpRequest.setRequestHeader() throws NS_ERROR_FAILURE inappropriately"
---
An exception code thrown by the [`XMLHttpRequest.setRequestHeader`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest#setRequestHeader) function was previously `NS_ERROR_FAILURE` regardless of the error. Two exception codes defined in the spec, `NS_ERROR_DOM_INVALID_STATE_ERR` and `NS_ERROR_DOM_SYNTAX_ERR`, are now used to make sure those errors can be clearly distinguished.
