---
title: "Errors on colours and lengths are now only allowed for specific properties"
date: "2012-12-03T03:50:54-05:00"
categories: ["css"]
tags: []
versions: ["17"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=774122"
      title: "Bug 774122 – limit CSS parser hashless-color and unitless-length quirks to only the properties that need them"
---
In Firefox's [Quirks (backward compatible) mode](https://developer.mozilla.org/en-US/docs/Mozilla_Quirks_Mode_Behavior), hashless colour codes like `666666`, not `#666666`, and unitless lengths like `10`, not `10px`, are automatically corrected by the CSS parser if such errors are found in the value of properties except shorthands. The Firefox implementation has been updated to allow such errors only for specific properties to follow the CSS3 spec.

For example, hashless colour codes are only allowed in the value of the [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color), [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color), [`border-top-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-color), [`border-right-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-color), [`border-bottom-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-color), [`border-left-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-color) and [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color) properties, while the value of the other properties like [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) or [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) won't be corrected. Anyway, you should fix your errors yourself.
