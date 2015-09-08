---
title: "Image maps are now displayed as inline elements"
date: "2012-12-03T03:50:54-05:00"
categories: ["css"]
tags: []
versions: "17"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=607267": "Bug 607267 – Image maps are display:block, but the HTML spec says they should be inline"
---
Image maps (the [`<map>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map) elements), previously displayed as [block elements](https://developer.mozilla.org/en-US/docs/HTML/Block-level_elements) in Firefox's Standard Compliant mode, are now displayed as [inline elements](https://developer.mozilla.org/en-US/docs/HTML/Inline_elements) to follow the [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5) spec. So far, those have been displayed as inline elements in the [Quirks (backward compatible) mode](https://developer.mozilla.org/en-US/docs/Mozilla_Quirks_Mode_Behavior) and on the other browsers. If you'd like to display image maps as block elements as before, you have to add `map { display: block; }` to your stylesheet.
