---
title: "`-moz-use-text-color` CSS colour keyword has been dropped"
date: "2016-10-03T17:30:00-04:00"
categories: ["css"]
tags: []
versions: ["52", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1306214"
      title: "Bug 1306214 - Remove -moz-use-text-color from color properties"
---
The support for the non-standard `-moz-use-text-color` CSS colour keyword, which could be used for the [`border-color`](https://developer.mozilla.org/docs/Web/CSS/border-color), [`outline-color`](https://developer.mozilla.org/docs/Web/CSS/outline-color) and several other properties, has been removed. Use the standardized [`currentcolor`](https://developer.mozilla.org/docs/Web/CSS/color_value#currentColor_keyword) keyword instead.
