---
title: "Most of Firefox-specific `-moz-appearance` values have been removed"
date: "2018-10-23T10:25:00-04:00"
categories: ["css"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496720"
      title: "Bug 1496720 - [css-compat] Unship -moz/webkit-appearance values not supported by other UAs / spec"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/odBz2i8xnno/discussion"
      title: "Intent to unship: most -moz-appearance values not supported by other UAs / spec"
---
Firefox 64 has removed the most of [`-moz-appearance`](https://developer.mozilla.org/docs/Web/CSS/appearance) CSS property values that are not supported by other browsers nor standardized in the spec. Those were mostly for internal use within the Firefox user interface written in now-deprecated [XUL](https://developer.mozilla.org/docs/Mozilla/Tech/XUL). Given that the `-webkit-appearance` property has been supported as an alias of `-moz-appearance` since Firefox 63, this removal affects `-webkit-appearance` as well.

The [removed values](https://hg.mozilla.org/try/diff/05e54dac9610/layout/style/test/test_non_content_accessible_values.html) include `radio-container`, `window` and `menulist-text`, which were the [most used values](https://bugzilla.mozilla.org/show_bug.cgi?id=1496720#c14) according to Mozilla developers. The [remaining values](https://compat.spec.whatwg.org/#css-non-aliased) include `none`, which is often used to disable the default style of native form widgets.
