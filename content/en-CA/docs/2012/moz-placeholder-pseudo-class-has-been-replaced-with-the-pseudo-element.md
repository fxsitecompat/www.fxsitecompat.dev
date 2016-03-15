---
title: "`:-moz-placeholder` pseudo-class has been replaced with the pseudo-element"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=737786"
      title: "Bug 737786 – Switch from :-moz-placeholder to ::-moz-placeholder (pseudo-class to pseudo-element)"
---
The [`:-moz-placeholder`](https://developer.mozilla.org/en-US/docs/Web/CSS/:-moz-placeholder) pseudo-class that matches form elements with the [`placeholder`](https://developer.mozilla.org/en-US/docs/Web/HTML/Forms_in_HTML#The_placeholder_attribute) attribute has been removed, and the [`::-moz-placeholder`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-moz-placeholder) pseudo-element has been added instead. The implementation of WebKit has been a pseudo-element, and this change is a part of the standardization effort.
