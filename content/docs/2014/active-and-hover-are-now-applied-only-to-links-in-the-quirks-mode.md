---
title: "`:active` and `:hover` are now applied only to links in the Quirks mode"
date: "2014-12-19T11:15:21-05:00"
categories: ["css"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=783213"
      title: "Bug 783213 – :active and :hover quirk should only apply to links"
---
Previously, the [`:active`](https://developer.mozilla.org/docs/Web/CSS/:active) and [`:hover`](https://developer.mozilla.org/docs/Web/CSS/:hover) pseudo-classes could be applied to not only links but also images and [form controls](https://developer.mozilla.org/docs/Web/Guide/HTML/Forms_in_HTML) if the page is rendered in the [Quirks mode](https://developer.mozilla.org/docs/Mozilla_Quirks_Mode_Behavior). This behaviour has been corrected to align with the spec and other browsers. See a [comment in the bug](https://bugzilla.mozilla.org/show_bug.cgi?id=783213#c31) for more details on this change.
