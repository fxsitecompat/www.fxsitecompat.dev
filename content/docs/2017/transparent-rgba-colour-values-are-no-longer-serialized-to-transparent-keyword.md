---
title: "Transparent RGBA colour values are no longer serialized to `transparent` keyword"
date: "2017-02-21T18:30:00-05:00"
categories: ["css", "dom"]
tags: []
versions: ["54"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1339394"
      title: "Bug 1339394 - Don't serialize transparent colors to \"transparent\" keyword in various cases"
---
Previously, Firefox was wrongly serializing `rgba(0, 0, 0, 0)` to the `transparent` keyword for the [specified value](https://developer.mozilla.org/docs/Web/CSS/specified_value) that could be retrieved with the [`HTMLElement.prototype.style`](https://developer.mozilla.org/docs/Web/API/HTMLElement/style) property. Also, any colour value with zero alpha channel was being serialized to `transparent` for the [resolved value](https://developer.mozilla.org/docs/Web/CSS/resolved_value) returned by the [`window.getComputedStyle`](https://developer.mozilla.org/docs/Web/API/Window/getComputedStyle) method.

This bug has been fixed with Firefox 54 since it didn't match the spec nor other browsers' behaviour.
