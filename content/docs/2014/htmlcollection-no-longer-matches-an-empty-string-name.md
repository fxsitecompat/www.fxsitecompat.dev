---
title: "`HTMLCollection` no longer matches an empty string name"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=891952"
      title: "Bug 891952 – Update empty string handling in named getters to spec changes"
---
Previously, the empty named property of an [`HTMLCollection`](https://developer.mozilla.org/docs/Web/API/HTMLCollection) object, like `document.forms[0][""]`, was returning the first unnamed child element. This behaviour has been changed to return `undefined` to match the updated spec.
