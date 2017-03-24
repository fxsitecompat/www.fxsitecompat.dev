---
title: "CSS transitions may not work smoothly when `opacity` is used with other property"
date: "2017-03-21T19:50:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1318697"
      title: "Bug 1318697 - Elements disappear after sliding in"
---
Firefox 52 has introduced a regression where [CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions) are not applied as specified when the `opacity` property is changed at the same time as other certain property such as `transform` or `visibility`. The affected elements may flicker during the transition or disappear shortly. This bug has been fixed with Firefox 53 Beta.

**Update**: This bug has been fixed with Firefox 52.0.2.
