---
title: "`<label>` no longer has `form` attribute"
date: "2016-06-03T04:39:00-04:00"
categories: ["dom", "html"]
tags: []
releases: ["49", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268852"
      title: "Bug 1268852 - Spec change: Remove <label form> and redefine label.form IDL attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8TyeUQOn6qQ/discussion"
      title: "Intent to implement and ship: spec changes to the .form property and \"form\" attribute on <label> elements"
---
The [`<label>`](https://developer.mozilla.org/docs/Web/HTML/Element/label) element is no longer associated with any `<form>` according to the latest HTML spec. The support for the `form` attribute on `<label>`, introduced with HTML5, has been removed with Firefox 49 accordingly.

The `form` property on [`HTMLLabelElement`](https://developer.mozilla.org/docs/Web/API/HTMLLabelElement) DOM instances will instead return the labelled control's `form` property if any, and `null` otherwise. In other words, `label.form` will be an alias of `label.control.form`.
