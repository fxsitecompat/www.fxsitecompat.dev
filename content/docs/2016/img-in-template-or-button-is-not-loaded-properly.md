---
title: "`<img>` in `<template>` or `<button>` is not loaded properly"
date: "2016-12-04T21:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317901"
      title: "Bug 1317901 - Cloned images from <template> do not load."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1318889"
      title: "Bug 1318889 - SVG inside <img> is not displayed in Firefox 50"
aliases:
    - "/en-CA/docs/2016/img-in-template-will-not-be-loaded-when-added-to-document/"
---
Firefox 50 has introduced a regression where images defined within a [`<template>`](https://developer.mozilla.org/docs/Web/HTML/Element/template) are not loaded properly when the `<img>` elements are cloned from the template content and added to somewhere in the active document. An `<img>` within a `<button>` is also not loaded due to the same regression. Those failed `<img>`s will instead show the alternative text if specified. This bug has been fixed with Firefox 50.1.0.
