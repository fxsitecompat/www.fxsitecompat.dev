---
title: "`justify-items:auto` has been renamed to `legacy`"
date: "2018-05-07T19:25:00-04:00"
categories: ["css"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1363875"
      title: "Bug 1363875 - [css-align] Rename `auto` to `legacy` for `justify-items`"
---
Previously, the initial value for the [`justify-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-items) CSS property was `auto`. After a [discussion](https://github.com/w3c/csswg-drafts/issues/1318) in the CSS Working Group, it has been renamed to `legacy`. Firefox 61 makes this change as per the latest Box Alignment spec, making `auto` an invalid value with no transition period. Use `legacy` instead from now on.
