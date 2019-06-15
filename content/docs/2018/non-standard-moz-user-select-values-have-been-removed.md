---
title: "Non-standard `-moz-user-select` values have been removed"
date: "2018-11-21T17:08:00-05:00"
categories: ["css"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492958"
      title: "Bug 1492958 - [css-ui] Unship -moz/webkit-user-select values not supported by other UAs / spec"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/XfKl9Jt7ZQ8/discussion"
      title: "Intent to implement and ship: Unprefix -moz-user-select, unship mozilla-specific values."
---
The following Firefox-specific values have been removed from the [`-moz-user-select`](https://developer.mozilla.org/docs/Web/CSS/user-select) CSS property and its `-webkit-user-select` alias:

* `-moz-all`: Use `all` instead
* `-moz-text`: Use `text` instead
* `element`, `elements`, `toggle`, `tri-state`: These were unimplemented

In the near future, `-moz-none` will also be removed and the property will be unprefixed.

**Update**: The property has been unprefixed with [Firefox 69](https://www.fxsitecompat.dev/en-CA/docs/2018/non-standard-moz-user-select-values-have-been-removed/).
