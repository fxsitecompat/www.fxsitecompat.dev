---
title: "`RegExp.multiline` global switch has been deprecated"
date: "2015-12-19T00:43:00-05:00"
categories: ["javascript"]
tags: []
versions: ["46"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1220457"
      title: "Bug 1220457 - Show deprecation warning for non-standard RegExp.multiline."
---
The non-standard `multiline` property on the [`RegExp`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) object, that changes the multiline option of new regular Expressions, is considered deprecated and will be [removed in the near future](https://www.fxsitecompat.dev/en-CA/docs/2015/regexp-multiline-global-switch-will-be-removed/). Starting with Firefox 46, the Web Console shows a deprecation warning for this property. Use the `m` flag for the `RegExp` literal and constructor instead. Note that the standard [`multiline`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp/multiline) property on `RegExp` instances won't be removed.

**Update**: The support for the property has been [removed with Firefox 48](https://www.fxsitecompat.dev/en-CA/docs/2016/regexp-multiline-global-switch-has-been-removed/).
