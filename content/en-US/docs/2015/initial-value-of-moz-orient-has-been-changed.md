---
title: "Initial value of `-moz-orient` has been changed"
date: "2015-04-27T13:17:23-04:00"
categories: ["css"]
tags: []
versions: "40"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1028716": "Bug 1028716 – update values of -moz-orient for <progress> and <meter> to remove \'auto\', and add \'inline\' (new initial value) and \'block\' values with writing-mode support"
---
The implementation of the [`-moz-orient`](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-orient) property, that can be applied to the [`<progress>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress) and [`<meter>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter) elements, has been updated for the latest specification to support the [`writing-mode`](https://developer.mozilla.org/en-US/docs/Web/CSS/writing-mode) property on those elements. The initial `auto` value has been removed, while `inline`, the new initial value, and `block` are added as the possible values.
